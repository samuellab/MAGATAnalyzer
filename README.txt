Multi Animal Gait And Track Analyzer software

This code is hosted at https://github.com/samuellab/MAGATAnalyzer
The latest version may always be found here.  

This software requires MATLAB R2010a or later. It was developed with access to the full suite of MATLAB add-on packages.  Some of these packages may be required to run the software.  If you get undefined function errors, the likely cause is a missing package.  (If you do not have the mapping toolkit, the functions rad2deg and deg2rad are available in this repository and must be added to the matlab path.  One way to do this is to copy them into the basic routines directory of Matlab-Track-Analysis)

To run the labview VIs (not required to use software), you must have Labview 8.5 or later and the Vision Development Module.  

The MAGAT Analyzer includes 3 submodules
(1) track extraction software (to pull larval tracks from image stacks)

(2) Matlab-Track-Analysis (to extract behavioral metrics from larval tracks)

(3) Example Data (zipped file containing movies from 3 experiments with larvae navigating an Ethyl Acetate gradient in LADY GAGA - the Linear And Dynamic Gaseous Gradient Apparatus) If you downloaded this software from the Nature Methods website, the example data is not included.  

software is contained in submodules;  to load submodules, open git bash, change to this directory, then type

git submodule init
followed by
git submodule update

**IMPORTANT**
you must copy the openCV DLLs to your system path directory. They are in a folder titled "openCV dlls; copy to windows system32"
Copy to windows/system32 and windows/system just to be sure

To see an example of software use (takes about an hour for the first run on a standard desktop computer), 

(1)open matlab

(2) change to the Matlab-Track-Analysis directory 
cd (path to this directory)/Matlab-Track-Analysis

(3) type the command:
MAGAT_ANALYZER_START_HERE

Note that to use the matlab software, you must be in the matlab-track-analysis directory (in matlab) and first run the SetupDirectories command (this is done automatically by the MAGAT_ANALYZER_START_HERE command)

**The track extraction will run during the MATLAB session; You will see the message "when the track extraction software has finished running, this script will continue," and windows will open displays showing extraction progress. This will take 30+ minutes. If the software continues immediately, this indicates a problem running extract-stack.exe & is most likely due to a problem with the DLLs.

NB: Track Extraction Software contains submodules as well.  Though not required to run software, to get the full source code you must type

cd Track-Extraction-Software
git submodule init
git submodule update

cd Image-Stack-Compressor
git submodule init
git submodule update


**updated 11/16/2018 with minor bug fixes to address incompatabilities with newer versions of MATLAB
**README updated 11/16/2018 to include note to copy openCV DLLs to folder

LICENSE

Unless otherwise noted in the file, all code is copyright 2011 by Marc Gershow and is licensed under the Creative Commons Attribution Share Alike 3.0 United States License.
To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/3.0/us/ or send a letter to Creative Commons, 171 Second Street, Suite 300, San Francisco, California, 94105, USA.
Any modification or redistribution of this work must include this license.

If this work or its derivatives result in any reports or publications, you must acknowledge this work in the typical format.  Please cite:
Gershow M, Berck M, Mathew D, Luo L, Kane E, Carlson J, Samuel ADT. Controlling Airborne Chemical Cues For Studying Navigation in Small Animals. Nature Methods. 2012

*THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
**The author is under no obligation to provide any services by way of maintenance, updates or corrections for this software.  Nor is the author obligated to provide technical support or any form of assistance using this software.

Note that the creative commons license contains additional disclaimers and limitations on liability.  


The following are copyright/licensed by other individuals:
Where applicable modifications are copyright Marc Gershow and licensed under the same terms as the original source license.

YamlMatlab, by  
 - Jiri Cigler, Dept. of Control Engineering, CTU Prague
 - Jan  Siroky, Energocentrum PLUS s.r.o.
 MIT license
 http://code.google.com/p/yamlmatlab/

 SnakeYaml, by
 - Andrey Somov <py4fun@gmail.com>
 - Alexander Maslov
 Apache 2.0 license
 http://code.google.com/p/snakeyaml/

 barweb.m and barweb_marc.m (bar plot with error bars)
 Bolu Ajiboye (modified by Marc Gershow)
 BSD license
 http://www.mathworks.com/matlabcentral/fileexchange/10803

 assignApplicable, assignToStruct, assignFromStruct modified by Marc Gershow from
 pvpmod.m by U. Egert, H. Hentschke
 BSD license
 http://www.mathworks.com/matlabcentral/fileexchange/6190-abfload/content/pvpmod.m

 derivest suite
 John D'Errico 
 BSD license
 http://www.mathworks.com/matlabcentral/fileexchange/13490-adaptive-robust-numerical-differentiation

OpenCV
http://opencv.willowgarage.com/wiki/
BSD license
*from the BSD 3.0 license
** adapted from Albrecht and Bargmann, Nature Methods 8,599–605 (2011) doi:10.1038/nmeth.1630

