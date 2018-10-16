'''
/**
*  struct ListNode {
*        int val;
*        struct ListNode *next;
*        ListNode(int x) :
*              val(x), next(NULL) {
*        }
*  };
*/
class Solution {
public:
    vector<int> printListFromTailToHead(ListNode* head) {
        ListNode *node = head;
        stack<int> st;
        int count = 0;
        while(node != NULL)
        {
            st.push(node->val);
            count++;
            node = node->next;
        }
        vector<int> ans(count);
        for(int i = 0;i<count;i++){
            ans[i] = st.top( );
            st.pop( );
        }
        return ans;
    }
};


'''
