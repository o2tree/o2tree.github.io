# o2tree.github.io

- http://linktr.ee/o2tr
- http://tr.ee/UG_IGJ3t3a
- http://o2tree.carrd.co

- https://github.com/o2tree/o2tree.github.io/tree/main

- https://o2tree-carrd-co.translate.goog/?_x_tr_sl=auto&_x_tr_tl=id&_x_tr_hl=en
- https://o2tree-carrd-co.translate.goog/?_x_tr_sl=en&_x_tr_tl=id&_x_tr_hl=en

- https://www.maps.ie/coordinates.html

- https://www.google.com/maps/place/-1.6000944282676468+103.63552987575531/@-1.6000944282676468,103.63552987575531,17z

- [Culture polychaete - cacing Nipah as feed](https://www.bluelifehub.com/2023/04/18/polychaete-farming-as-a-valuable-sustainable-opportunity-in-aquaculture/)
- [culture polychaete - India](https://bioticapublications.com/journal-backend/articlePdf/421a7f7e27.pdf)
- [culture polychaete - 3](http://panamjas.org/pdf_artigos/PANAMJAS_8(2)_142-146.pdf)
- https://polychaeta.net/en/
https://umaine.edu/cooperative-aquaculture/wp-content/uploads/sites/75/2015/11/Waste-to-worms.jpg


Jln Orang Kayu Pingai No. 49 

RT026/RW08

Jambi, Jambi Timur 36142

0 822 8912 8535



mkdir .github/actions/ansible

--- Dockerfile: ----

FROM  <DockerHub-UserName>/ansible-in-containers

COPY ./entrypoint.sh /entrypoint.sh

ENTRYPOINT ["bash","/entrypoint.sh"]




Create a new Dockerfile.



FROM  <DockerHub-UserName>/ansible-in-containers

COPY ./entrypoint.sh /entrypoint.sh

ENTRYPOINT ["bash","/entrypoint.sh"]


Copy the entrypoint.sh script to the Ansible Action directory.


--- entrypoint.sh---
#BASH
Copy entrypoint.sh .github/actions/ansible

#POWERSHELL
Copy-Item entrypoint.sh .github/actions/ansible

--- action.yml---------------

name: 'Ansible'
description: 'Runs an Ansible playbook'
inputs:
  playbook:
    description: 'Ansible playbook to run'
    required: true
    default: playbook.yml
  inventory:
    description: 'Ansible inventory to use'
    required: true
    default: localhost
runs:
  using: 'docker'
  image: 'Dockerfile'
  args:
    - ${{ inputs.playbook }}
    - ${{ inputs.inventory }}




</p>