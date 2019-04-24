# Nano (cryptocurrency) ansible scripts [WIP]

**Some ansible script to enable deployment of a nano node on IPv6 only node. For example Scaleway.**

1. Add inventory file

    Add a file named inventory to the root with the following conent
    
    IP = the IPv6 of your node. For example 2001:bc8:4455:2721::1583
    ```
    [nano_node]
    # Hosts list for installing the nano_node on
    nano_node ansible_host=IP ansible_connection=ssh ansible_user=root
    ```

2. Execute the ansible playbook

    ```bash
    ansible-playbook -i inventory -v site.yml
    ```
