c-index
=======
Quantifying computational research impact through contributions


Usage
------

Install [PyGithub](https://github.com/PyGithub/PyGithub):
```
pip install pygithub
```
Get authorization token from GitHub:

[Personal API tokens](https://github.com/blog/1509-personal-api-tokens)

See `github-api.ipynb` for more information.

### Example

```python
from github import Github

auth_token = ''
git = Github(auth_token)

user_name = 'wilmerlab'
repo_name = 'my_repo'
user = git.get_user(user_name)
repo = user.get_repo(repo_name)

print('Forks: %i | Watchers: %i | Stars: %i' % (repo.forks_count, repo.watchers_count, repo.stargazers_count))

 >>> Forks: 4 | Watchers: 3 | Stars: 3
```
