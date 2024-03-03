class Solution{
public:
      static bool comp(string a, string b){
	    string ab=a.append(b);
	    string ba=b.append(a);
	    
	    return ab.compare(ba)>0?1:0;
      }
	// The main function that returns the arrangement with the largest value as
	// string.
	// The function accepts a vector of strings
	string printLargest(int n, vector<string> &arr) {
	    // code here
	      sort(arr.begin(), arr.end(), comp);
	    
	    string a="";
	    for(int i=0;i<n;i++){
	        a+=arr[i];
	    }
	    return a;
	}
};
