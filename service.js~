(function(){

    'use strict';

    var myService = angular.module('Demo').service('Item', Itemservice);

    function Itemservice($filter, Utils)
    {
        var service = {};
        var emptyGroupe = {
           //composite
            uid: undefined,
            email: undefined,
            childrenId: [],
            // Groupe
            name: undefined,
          
        };
        
        var emptyUser = {
           //composite
            uid: undefined,
            email: undefined,
            childrenId: [],
            // 
            lastname: undefined,
            firstname: undefined,
            tel: undefined,  
        };


        var list = [];


/*
         {
                creationDate: new Date(),
                lastModificationDate: new Date(),
                items: [],
                uid: 'abc',
                tag: 'test',
                title: 'Note avec tag test',
                text: 'test',
                type: 'text',
                status: 'live'
            }, {
                creationDate: new Date(),
                lastModificationDate: new Date(),
                items: [],
                uid: 'def',
                tag: undefined,
                title: 'Note sans tag',
                text: 'test',
                type: 'text',
                status: 'live'
            }, {
                creationDate: new Date(),
                lastModificationDate: new Date(),
                items: [
                    { text: 'Pain', checked: false },
                    { text: 'Farine', checked: true },
                    { text: 'Chocolat', checked: false }
                ],
                uid: 'def',
                tag: undefined,
                title: 'Liste de course sans tag',
                text: 'test',
                type: 'list',
                status: 'live'
            }, {
                creationDate: new Date(),
                lastModificationDate: new Date(),
                items: [],
                uid: 'ghi',
                tag: 'test',
                title: 'Note avec encore tag test',
                text: 'test',
                type: 'text',
                status: 'live'
            }, {
                creationDate: new Date(),
                lastModificationDate: new Date(),
                items: [],
                uid: 'jkl',
                tag: 'autre tag',
                title: 'Note avec un autre tag',
                text: 'test',
                type: 'text',
                status: 'live'
            },
*/
        service.del = del;
        service.get = get;
        service.List = List;
        service.create = create;
        service.save = save;

        //////////

        function del(item)
        {
            list = $filter('filter')(list, { uid: "!" + item.uid });
            //list = $filter('filter')(list, { childrend.id:  item.uid });
        }

        function get(uid)
        {
            var filteredList = $filter('filter')(list, { uid: item.uid });
            return filteredList[0];
        }

        function List()
        {
            return list;
        }


        function create(test)
        {

       if(test="0"){
            var newItem = angular.copy(emptyUser);
            newUser.uid = Utils.generateUUID();
            
           }
        else{
            var newItem = angular.copy(emptyGroup);
            newItem.uid = Utils.generateUUID();
        }
            return newItem;
     }

        function save(item)
        {
            //note.lastModificationDate = new Date();
            for (var idx in list)
            {
                if (list[idx].uid === item.uid)
                {
                    list[idx] = item;
                    return;
                }
            }

            list.push(item);
        }
        return service;
    }

})();
