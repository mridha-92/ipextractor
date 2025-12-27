# ipextractor
Introducing a Bash tool designed to efficiently extract IP addresses from a list of subdomains. This tool supports multiple DNS query methods and parallel processing for faster results, making it a valuable asset for security assessments and network analysis.


./ipextractor.sh -h                                                        
Usage: ./ipextractor.sh [OPTIONS] <subdomains_file>

Options:
  -o, --output FILE     Output file (default: ips_<timestamp>.txt)
  -t, --threads NUM     Number of concurrent threads (default: 10)
  -d, --dns-server IP   DNS server to use (default: 8.8.8.8)
  -c, --csv             Output in CSV format (subdomain,ip)
  -j, --json            Output in JSON format
  -s, --summary         Show summary only (no detailed output)
  -h, --help            Show this help message

Examples:
  ./ipextractor.sh subdomains.txt
  ./ipextractor.sh -t 20 -o results.txt subdomains.txt
  ./ipextractor.sh -c -d 1.1.1.1 subdomains.txt
