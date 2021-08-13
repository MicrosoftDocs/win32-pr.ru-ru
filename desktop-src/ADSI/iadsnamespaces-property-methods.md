---
title: Методы свойств Иадснамеспацес (iAds. h)
description: Методы свойств интерфейса Иадснамеспацес получают и задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадснамеспацес ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8daeed67202add437ee06b9905cbd70a0c202863c476155216f2340be1c7b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691432"
---
# <a name="iadsnamespaces-property-methods"></a>Методы свойств Иадснамеспацес

Методы свойств интерфейса [**иадснамеспацес**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) получают и задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**DefaultContainer**
</dt> <dd> <dl>

Свойство **дефаултконтаинер** определяет базовый объект контейнера, к которому можно выполнить привязку и использовать в качестве отправной точки при просмотре. Эти данные хранятся и извлекаются из следующего значения реестра.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

ADSI определяет свойство **дефаултконтаинер** , чтобы обеспечить быстрый способ получения указателя на ранее определенный объект контейнера ADSI.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Remarks

Поставщики должны предоставлять это свойство для каждого пользователя. Контейнер по умолчанию задается сразу после вызова **иадснамеспацес::p UT \_ дефаултконтаинер**. Вызов метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) не требуется. На самом деле объект, предоставляемый системой пространств имен, возвращает **E \_ нотимпл** для метода **iAds. сетинфо** , вызываемого для этого объекта. Если контейнер является объектом namespaces, операция перечисления всегда приводит к получению списка объектов пространства имен, относящихся к поставщику. Если для получения объекта пространства имен используется [**иадсконтаинер. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) , параметр *бстркласс* игнорируется. Это связано с тем, что контейнер, то есть объект namespaces, содержит только один тип объекта, а именно, объекты пространства имен, относящиеся к поставщику.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадснамеспацес определен как 28B96BA0-B330-11CF-A9AD-00AA006BC149<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Иадсконтаинер. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[**иадснамеспацес**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[Методы свойств интерфейса](interface-property-methods.md)
</dt> </dl>

 

 





