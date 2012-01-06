A simple script for sending messages to scribe. this is working like tail commands.

# Usage

    $ scribe_tail --help
    usage: scribe_tail [-h] [-v] -c CATEGORY [-l HOST] [-p PORT] [--rewind REWIND]
                       [--follow_delay FOLLOW_DELAY]
                       [--read_line_buf_size READ_LINE_BUF_SIZE]
                       [--flush_interval FLUSH_INTERVAL]
                       [--fail_store_path FAIL_STORE_PATH]
                       [--fail_store_mb_per_file FAIL_STORE_MB_PER_FILE]
                       [--fail_store_backup_count FAIL_STORE_BACKUP_COUNT]
                       FILE

    Follow file and send data to scribe.

    positional arguments:
      FILE                  target file name

    optional arguments:
      -h, --help            show this help message and exit
      -v, --version         show program's version number and exit
      -c CATEGORY, --category CATEGORY
                            scribe category
      -l HOST, --host HOST  scribe host (default: 127.0.0.1)
      -p PORT, --port PORT  scribe port (default: 1463)
      --rewind REWIND       start read the file from the beginning (default:
                            false)
      --follow_delay FOLLOW_DELAY
                            follow file delay(Sec) (default: 0.5)
      --read_line_buf_size READ_LINE_BUF_SIZE
                            read line buffer size (default: 100)
      --flush_interval FLUSH_INTERVAL
                            flush read line buffer interval(Sec) (default: 10.0)
      --fail_store_path FAIL_STORE_PATH
                            store path to write scribe send failed data (default:
                            same with FILE's directory)
      --fail_store_mb_per_file FAIL_STORE_MB_PER_FILE
                            fail store file size(MB) (default: 200)
      --fail_store_backup_count FAIL_STORE_BACKUP_COUNT
                            fail store file backup count (default: 5)

    $ scribe_tail --category YOUT_SCRIBE_CATEGORY --host HOSTNAME --port 1463 --rewind=true FILE
