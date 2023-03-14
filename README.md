# Basics
## Vectors, matrices, <img src="svgs/f3e711926cecfed3003f9ae341f3d92b.svg?invert_in_darkmode" align=middle width=11.87217899999999pt height=22.648391699999998pt/> ... Oh my!
An <img src="svgs/55a049b8f161ae7cfeb0197d75aff967.svg?invert_in_darkmode" align=middle width=9.86687624999999pt height=14.15524440000002pt/> dimensional vector, where the number of elements in the vector is indicated by <img src="svgs/55a049b8f161ae7cfeb0197d75aff967.svg?invert_in_darkmode" align=middle width=9.86687624999999pt height=14.15524440000002pt/>, is written in the following form:
<p align="center"><img src="svgs/f41cbc76fbb2b9cde4cb62b460466a9a.svg?invert_in_darkmode" align=middle width=287.35877445pt height=16.438356pt/></p> 

The amount of dimensions spanned by the vector is indicated by <img src="svgs/8a86f4a11e2fbfc03de61d587ba826de.svg?invert_in_darkmode" align=middle width=19.998202949999992pt height=22.648391699999998pt/>, such as <img src="svgs/c96f2a7298e342fdacc24044839bc4a6.svg?invert_in_darkmode" align=middle width=18.424726649999986pt height=26.76175259999998pt/>,<img src="svgs/433badc501d4f8a183b14684b47f305e.svg?invert_in_darkmode" align=middle width=18.424726649999986pt height=26.76175259999998pt/>, <img src="svgs/d03c1e146df015e061405cc425738d83.svg?invert_in_darkmode" align=middle width=18.424726649999986pt height=26.76175259999998pt/>.

Matrices are arrangements of numbers into rows and columns, used when solving systems of linear equations. The size of the matrix is written as a matrix row <img src="svgs/bdbf342b57819773421273d508dba586.svg?invert_in_darkmode" align=middle width=12.785434199999989pt height=19.1781018pt/> column vector. Usually <img src="svgs/4afc093f95ae3f3a5a07f032a64b0a26.svg?invert_in_darkmode" align=middle width=44.39116769999999pt height=19.1781018pt/>. Two <img src="svgs/ab2d2968f149e290d718f3d1135e40ac.svg?invert_in_darkmode" align=middle width=36.52961069999999pt height=21.18721440000001pt/> vectors are written as:
<p align="center"><img src="svgs/e4c2988099c8dead38c49da236f1a656.svg?invert_in_darkmode" align=middle width=185.18817735pt height=39.452455349999994pt/></p>
Matrices are used in the solving of systems of linear equations, where the following system is written in the indicated form:
<p align="center"><img src="svgs/9e28490d8efd0808347bb7bdb4524824.svg?invert_in_darkmode" align=middle width=272.07361005pt height=39.452455349999994pt/></p>

## Working with vectors and matrices
### Vectors

dot product / inner product: 
<p align="center"><img src="svgs/d845de26c3dcf9dba830ec99d73ae3b7.svg?invert_in_darkmode" align=middle width=401.92691879999995pt height=44.89738935pt/></p>
cross product results in a vector that is perpendicular to the two vectors:
<p align="center"><img src="svgs/d3464d235941af04acb0d469fa7402b4.svg?invert_in_darkmode" align=middle width=358.47874095pt height=59.1786591pt/></p>
norms:
<p align="center"><img src="svgs/ace0771f444e7b77070c77d3e2f9f160.svg?invert_in_darkmode" align=middle width=136.86357794999998pt height=59.17867724999999pt/></p>
<p align="center"><img src="svgs/10484d189ac9d3532a8768958816417b.svg?invert_in_darkmode" align=middle width=186.79674255pt height=44.89738935pt/></p>
<p align="center"><img src="svgs/94d27f3b2b4ae1e0f030981606f03921.svg?invert_in_darkmode" align=middle width=193.34929019999998pt height=44.89738935pt/></p>
<p align="center"><img src="svgs/d1181df5b94c74cdba50e55b991bd890.svg?invert_in_darkmode" align=middle width=119.01161909999999pt height=22.68260445pt/></p>

### Matrices
* Matrix multiplication is associative: <img src="svgs/5fde458f61e9690bc0bf0fbcdce84a93.svg?invert_in_darkmode" align=middle width=124.58217749999997pt height=24.65753399999998pt/>
* Matrix operations are distributive: <img src="svgs/2361fda5610816360f5a16df6bfa7b38.svg?invert_in_darkmode" align=middle width=164.3079306pt height=24.65753399999998pt/> and <img src="svgs/89b4982ff093e641faad0b4fa252ffa3.svg?invert_in_darkmode" align=middle width=169.52022119999998pt height=24.65753399999998pt/>.
* Matrix multiplication is not commutative: Usually <img src="svgs/d4125d316988b103818ac55c042a2e94.svg?invert_in_darkmode" align=middle width=73.16203454999999pt height=22.831056599999986pt/>

Matrices can only be multiplied if there are as many columns of <img src="svgs/53d147e7f3fe6e47ee05b88b166bd3f6.svg?invert_in_darkmode" align=middle width=12.32879834999999pt height=22.465723500000017pt/> as there are rows of <img src="svgs/61e84f854bc6258d4108d08d4c4a0852.svg?invert_in_darkmode" align=middle width=13.29340979999999pt height=22.465723500000017pt/>. I.e. if <img src="svgs/53d147e7f3fe6e47ee05b88b166bd3f6.svg?invert_in_darkmode" align=middle width=12.32879834999999pt height=22.465723500000017pt/> is of the size <img src="svgs/205995f88b807b2f5268f7ef4053f049.svg?invert_in_darkmode" align=middle width=44.39116769999999pt height=19.1781018pt/> and <img src="svgs/61e84f854bc6258d4108d08d4c4a0852.svg?invert_in_darkmode" align=middle width=13.29340979999999pt height=22.465723500000017pt/> is <img src="svgs/c0e991f2266d76861db938440931060c.svg?invert_in_darkmode" align=middle width=39.03343619999999pt height=22.831056599999986pt/>. 

dot product:
_what is dot product_?

<img src="svgs/f34558f6df686b5d2c8c7ae1b973dd32.svg?invert_in_darkmode" align=middle width=283.55761829999994pt height=47.6716218pt/>

cross product:
_what is cross product_?

<img src="svgs/2d21929e839fc884cc4c4ebd95fa42e0.svg?invert_in_darkmode" align=middle width=291.7768276499999pt height=47.6716218pt/>


transpose: <img src="svgs/03a2252f54526a4a19963bc07a0390dc.svg?invert_in_darkmode" align=middle width=97.37831399999999pt height=27.6567522pt/>: "mirror over main diagonal"
