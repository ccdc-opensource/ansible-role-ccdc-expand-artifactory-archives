# Ansible Role: ccdc.expand_artifactory_archives

Downloads archives from artifactory and expands them into the build machines.

See [Build machine provisioning](https://ccdc-cambridge.atlassian.net/l/c/u6inG791) on confluence for more information.

## Role Variables

## Example Playbook

    - hosts: all
      roles:
        - ccdc.expand_artifactory_archives
      vars:
        artifactory-archives:
          # Executables used by our software
          - artifactory_path: ccdc-3rdparty-windows-runtime-exes
            filename: fasta-36.3.8e.7z
            base_destination_directory: D:\x_mirror\buildman\tools\fasta
            # Move files out of a specific directory into the base_destination_directory
            # Can be used to keep specific directories or to remove a prefix in the archive
            move_and_delete_base_directory: fasta-36.3.8e


## License

MIT / BSD

## Author Information

This role was created in 2020 by Claudio Bantaloukas, based on existing roles at CCDC, by Jeff Geerling and google searches