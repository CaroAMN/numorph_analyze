FROM matlabruntime/r2023a/release/update5/f000c0002000000000

# Create the directory
RUN mkdir -p /usr/bin/mlrtapp

COPY /build/numorph_analyze /usr/bin/mlrtapp
COPY /build/run_numorph_analyze.sh /usr/bin/mlrtapp
COPY /build/readme.txt /usr/bin/mlrtapp

RUN chmod -R a+rX /usr/bin/mlrtapp/

# Set the MCR_CACHE_ROOT environment variable
ENV MCR_CACHE_ROOT=/tmp

# Add MATLAB app directory to PATH
ENV PATH="/usr/bin/mlrtapp:${PATH}"