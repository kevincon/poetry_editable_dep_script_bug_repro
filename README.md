Reproduced on Windows 10 Enterprise version 1909 build 18363.1139:

```sh
C:\Users\kevincon\repos\poetry_editable_dep_script_bug_repro 
λ poetry --version
Poetry version 1.1.3

C:\Users\kevincon\repos\poetry_editable_dep_script_bug_repro 
λ poetry install
Creating virtualenv parent-MPYm-h1y-py3.8 in C:\Users\kevincon\AppData\Local\pypoetry\Cache\virtualenvs
Installing dependencies from lock file

Package operations: 1 install, 0 updates, 0 removals

  • Installing child (0.1.0 C:/Users/kevincon/repos/poetry_editable_dep_script_bug_repro/child)

Installing the current project: parent (0.1.0)

C:\Users\kevincon\repos\poetry_editable_dep_script_bug_repro 
λ poetry run parent-cli
Hello from parent CLI!

C:\Users\kevincon\repos\poetry_editable_dep_script_bug_repro 
λ poetry run child-cli

  FileNotFoundError

  [WinError 2] The system cannot find the file specified

  at ~\AppData\Local\Programs\Python\Python38-32\lib\subprocess.py:1307 in _execute_child
      1303│             sys.audit("subprocess.Popen", executable, args, cwd, env)
      1304│
      1305│             # Start the process
      1306│             try:
    → 1307│                 hp, ht, pid, tid = _winapi.CreateProcess(executable, args,
      1308│                                          # no special security
      1309│                                          None, None,
      1310│                                          int(not close_fds),
      1311│                                          creationflags,
```
