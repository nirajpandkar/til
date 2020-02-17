# Wand image library policy error

**Problem**: Wand was giving the following error while reading PDF -

> wand.exceptions.PolicyError: not authorized

Apparently due to a [security fix]((https://bugs.launchpad.net/ubuntu/+source/imagemagick/+bug/1796563)) in ImageMagick library, the policies for ghostscript formats were disabled in the policy file residing in `/etc/ImageMagick-6/policy.xml`. 

**Solution**: Open the `policy.xml` file and change the attribute `rights` from `none` to `read`. 


### References

* [StackOverflow](https://stackoverflow.com/a/52701227/4411757)