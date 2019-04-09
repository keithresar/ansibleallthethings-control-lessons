# Creating a Credential

Credentials are utilized by Tower for authentication when launching Jobs against machines, synchronizing 
with inventory sources, and importing project content from a version control system.

You can grant users and teams the ability to use these credentials, without actually exposing the credential 
to the user. If you have a user move to a different team or leave the organization, you don’t have to re-key 
all of your systems just because that credential was available in Tower.

<hr>

### Exercise 4.2 Login to Ansible Tower

Connect to the workshop Ansible Tower instance and login using the username `admin` and password `ansible`.


### Exercise 4.3 Apply License

You should have received a license in your email (requested in exercise 4.1).  If you have not received one
get support from an instructor.

After logging into Ansible Tower you will have a prompt requesting the license.  
Browse the the license file you saved, agree to the EULA, and press submit.


### Exercise 4.4 Creating a Machine Credential

Machine credentials enable Tower to invoke Ansible on hosts under your management. Just like using Ansible on 
the command line, you can specify the SSH username, optionally provide a password, an SSH key, a key password, 
or even have Tower prompt the user for their password at deployment time. They define ssh and user-level privilege 
escalation access for playbooks, and are used when submitting jobs to run playbooks on a remote host.

Get started by navigating to the credentials page:

 - Click **Credentials** on lefthand sidebar
 - Click the green **plus** button to create a new credential

Add a new credential with the following properties:

 - **Name** - `Control Server` (replace with your unique student username)
 - **Credential Type** - Machine
 - **Username** - `studentX` (replace with your unique student username)
 - **Password** - Your unique password
 - *The remaining fields can be left as is*

Click **Save**.

<img src="/images/tower_credential.png" style="margin-left:2em; max-width: 80%; margin-bottom:1em;">

Verify who has access to this credential by clicking on the **Permissions** link.


### 📗 Resources

 - [Ansible Tower Credentials User Guide](http://docs.ansible.com/ansible-tower/latest/html/userguide/credentials.html)

