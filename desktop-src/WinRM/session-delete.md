---
title: Метод Session. redelete (Всмандисп. h)
description: Удаляет ресурс, указанный в URI ресурса.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Delete
- служба удаленного управления Windows метода Delete, объект Session
- объект Session служба удаленного управления Windows, метод Delete
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 769ef3f462fa542e9afc6859b564e1a32ed87578894df4008fb6a19ad8aadad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858674"
---
# <a name="sessiondelete-method"></a>Session. redelete, метод

Удаляет ресурс, указанный в URI ресурса.

## <a name="syntax"></a>Синтаксис


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*resourceUri* \[ окне\]
</dt> <dd>

URI ресурса, который необходимо удалить. Для указания ресурса можно также использовать объект [**ResourceLocator**](resourcelocator.md) .

</dd> <dt>

*Флаги* \[ в необязательное\]
</dt> <dd>

Зарезервировано для последующего использования. Должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Для вызова этого метода используется следующий синтаксис.


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a>Примеры

В следующем примере кода VBScript удаляются прослушиватели, настроенные для транспорта HTTP.


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Сеанс**](session.md)
</dt> </dl>

 

 





