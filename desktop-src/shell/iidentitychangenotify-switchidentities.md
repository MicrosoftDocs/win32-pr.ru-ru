---
description: Вызывается при переключении удостоверений пользователя.
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'Метод Иидентитичанженотифи:: Свитчидентитиес (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 925b52a4470c768501dd928784d85a89d05a90c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997666"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a>Метод Иидентитичанженотифи:: Свитчидентитиес

\[**Свитчидентитиес** доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен.\]

Вызывается при переключении удостоверений пользователя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Примечания

Этот метод можно реализовать, чтобы обеспечить пользовательское поведение приложения, когда пользователь успешно переключил удостоверения. Чтобы обеспечить пользовательское поведение перед переключением удостоверения пользователя, реализуйте метод [**иидентитичанженотифи:: куерисвитчидентитиес**](iidentitychangenotify-queryswitchidentities.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Окончание поддержки клиента<br/>    | Windows 2000 Professional<br/>                                                   |
| Поддержка конца сервера<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Мсидент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсидент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иидентитичанженотифи**](iidentitychangenotify.md)
</dt> <dt>

[**Иидентитичанженотифи:: Куерисвитчидентитиес**](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




