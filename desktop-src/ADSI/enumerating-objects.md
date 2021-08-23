---
title: Перечисление объектов
description: Чтобы просмотреть дочерний объект контейнера, например подразделения (OU), перечислите объект контейнера.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Перечисление объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e4bcead2d3fc8f98daeada89cdd10b3ad30bed855563efd89b3eebce8995f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961953"
---
# <a name="enumerating-objects"></a>Перечисление объектов

Чтобы просмотреть дочерний объект контейнера, например подразделения (OU), перечислите объект контейнера. Чтобы обеспечить аналогию в файловой системе, дочерний объект будет соответствовать файлам в каталоге, а контейнер, являющийся родительским объектом, будет соответствовать самому каталогу. Вы также можете использовать операцию Enumerate, если требуется получить родительский объект объекта.

При перечислении объекта фактически выполняется привязка к объекту в каталоге, а для каждого объекта возвращается интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .

В следующем примере кода показано, как перечислить дочерние элементы контейнера.


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



Можно фильтровать типы объектов, возвращаемых из перечисления. Например, чтобы отобразить только пользователей и группы, используйте следующий пример кода перед перечислением.


```VB
Ou.Filter = Array("user", "group")
```



Если имеется ссылка на объект, можно [**получить родительский**](/windows/desktop/api/Iads/nn-iads-iads) объект объекта с помощью свойства [**Parent**](iads-property-methods.md) . В следующем примере кода показано, как выполнить привязку к родительскому объекту.


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



Дополнительные сведения см. в разделе [Перечисление объектов ADSI](enumerating-adsi-objects.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поиск объектов](searching-for-objects.md)
</dt> </dl>

 

 




