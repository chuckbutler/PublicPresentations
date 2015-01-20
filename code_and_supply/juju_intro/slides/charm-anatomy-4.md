##  Charm Anatomy - Tests

```
    def test_docker_installation(self):
        """ Check if the docker binary is installed. """
        stat = self.docker_unit.file_stat('/usr/bin/docker')
        if not stat:
            amulet.raise_status(amulet.FAIL, msg='Docker binary missing!')
```


note:
    Put your speaker notes here.
    You can see them pressing 's'.
