This folder is Thi Ngo's individual task
---- Library setup ----
# Uninstall conflicting packages
!pip uninstall -y jax jaxlib flax numpy

# Install safe versions that work with Ray 2.9.0
!pip install "jax==0.4.23" "jaxlib==0.4.23" "flax==0.7.2"
!pip install "numpy==1.24.4"
!pip install "ray[rllib]==2.9.0"
!pip install "gym[atari]==0.26.2" ale-py==0.8.1

# Force reinstall of setuptools which includes pkg_resources
!pip install --force-reinstall "setuptools==65.5.0"

# Install gym atari + autoRom
!pip install "gym[atari]" "autorom[accept-rom-license]"
!AutoROM --accept-license
!pip install gym[atari] autorom[accept-rom-license]
!pip install gymnasium[atari]
