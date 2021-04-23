---
title: Перечисление объектов
description: Чтобы просмотреть дочерний объект контейнера, например подразделения (OU), перечислите объект контейнера.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Перечисление объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887556"
---
# <a name="enumerating-objects"></a><span data-ttu-id="9e3df-104">Перечисление объектов</span><span class="sxs-lookup"><span data-stu-id="9e3df-104">Enumerating Objects</span></span>

<span data-ttu-id="9e3df-105">Чтобы просмотреть дочерний объект контейнера, например подразделения (OU), перечислите объект контейнера.</span><span class="sxs-lookup"><span data-stu-id="9e3df-105">To view the child object of a container, such as an organizational unit (OU), enumerate the container object.</span></span> <span data-ttu-id="9e3df-106">Чтобы обеспечить аналогию в файловой системе, дочерний объект будет соответствовать файлам в каталоге, а контейнер, являющийся родительским объектом, будет соответствовать самому каталогу.</span><span class="sxs-lookup"><span data-stu-id="9e3df-106">To make an analogy to a file system, the child object would correspond to files in the directory, while the container, which is the parent object, would correspond to the directory itself.</span></span> <span data-ttu-id="9e3df-107">Вы также можете использовать операцию Enumerate, если требуется получить родительский объект объекта.</span><span class="sxs-lookup"><span data-stu-id="9e3df-107">You may also use the enumerate operation when you want to get the parent object of an object.</span></span>

<span data-ttu-id="9e3df-108">При перечислении объекта фактически выполняется привязка к объекту в каталоге, а для каждого объекта возвращается интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="9e3df-108">When you enumerate an object, you actually bind to an object in the directory, and an [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface is returned on each object.</span></span>

<span data-ttu-id="9e3df-109">В следующем примере кода показано, как перечислить дочерние элементы контейнера.</span><span class="sxs-lookup"><span data-stu-id="9e3df-109">The following code example shows how to enumerate the children of a container.</span></span>


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



<span data-ttu-id="9e3df-110">Можно фильтровать типы объектов, возвращаемых из перечисления.</span><span class="sxs-lookup"><span data-stu-id="9e3df-110">You can filter the types of objects returned from the enumeration.</span></span> <span data-ttu-id="9e3df-111">Например, чтобы отобразить только пользователей и группы, используйте следующий пример кода перед перечислением.</span><span class="sxs-lookup"><span data-stu-id="9e3df-111">For example, to display only users and groups, use the following code example before the enumeration.</span></span>


```VB
Ou.Filter = Array("user", "group")
```



<span data-ttu-id="9e3df-112">Если имеется ссылка на объект, можно [**получить родительский**](/windows/desktop/api/Iads/nn-iads-iads) объект объекта с помощью свойства [**Parent**](iads-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="9e3df-112">If you have an object reference, you can get the object's parent using the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) [**Parent**](iads-property-methods.md) property.</span></span> <span data-ttu-id="9e3df-113">В следующем примере кода показано, как выполнить привязку к родительскому объекту.</span><span class="sxs-lookup"><span data-stu-id="9e3df-113">The following code example shows how to bind to the parent object.</span></span>


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



<span data-ttu-id="9e3df-114">Дополнительные сведения см. в разделе [Перечисление объектов ADSI](enumerating-adsi-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9e3df-114">For more information, see [Enumerating ADSI Objects](enumerating-adsi-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e3df-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9e3df-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e3df-116">Поиск объектов</span><span class="sxs-lookup"><span data-stu-id="9e3df-116">Searching for Objects</span></span>](searching-for-objects.md)
</dt> </dl>

 

 




