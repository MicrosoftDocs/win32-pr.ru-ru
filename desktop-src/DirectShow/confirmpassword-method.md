---
description: Метод Двдадм. ConfirmPassword проверяет, соответствует ли указанный пароль ранее сохраненному паролю.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Метод ConfirmPassword (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668655"
---
# <a name="confirmpassword-method"></a>Метод ConfirmPassword

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`DVDAdm.ConfirmPassword`Метод проверяет, соответствует ли указанный пароль ранее сохраненному паролю.

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*сусернаме*
</dt> <dd>

Указывает имя пользователя в виде строки.

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*спассворд*
</dt> <dd>

Указывает новый пароль в виде строки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если указанный пароль совпадает с существующим паролем, и false в противном случае.

## <a name="remarks"></a>Комментарии

В настоящее время параметр *сусернаме* игнорируется на этом и всех связанных методах.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Сегмент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ChangePassword;**](changepassword-method.md)
</dt> <dt>

[Объект Мсдвдадм](msdvdadm-object.md)
</dt> </dl>

 

 




