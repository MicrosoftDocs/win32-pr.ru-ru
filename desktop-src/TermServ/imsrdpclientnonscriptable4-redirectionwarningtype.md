---
title: IMsRdpClientNonScriptable4 Редиректионварнингтипе, свойство
description: Управляет присутствием и внешним видом диалогового окна, которое уведомляет пользователя о перенаправлении.
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Редиректионварнингтипе
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681934"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a>Свойство IMsRdpClientNonScriptable4:: Редиректионварнингтипе

Управляет присутствием и внешним видом диалогового окна, которое уведомляет пользователя о перенаправлении.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a>Значение свойства

Задает тип диалогового окна, которое уведомляет пользователя о перенаправлении.

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**Редиректионварнингтипедефаулт** (символ 0x0000)


</dt> <dd>

Диалоговое окно не зависит от издателя.

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**Редиректионварнингтипеунсигнед** (0x0001)


</dt> <dd>

Диалоговое окно предназначено для неподписанных файлов.

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**Редиректионварнингтипеункновн** (0x0002)


</dt> <dd>

Диалоговое окно предназначено для неизвестного издателя.

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**Редиректионварнингтипеусер** (0x0003)


</dt> <dd>

Диалоговое окно предназначено для файлов пользователя.

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**Редиректионварнингтипесирдпартисигнед** (0x0004)


</dt> <dd>

Диалоговое окно отображается для файлов, сертифицированных сторонними компаниями и подписанных.

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**Редиректионварнингтипетрустед** (0x0005)


</dt> <dd>

Диалоговое окно не отображается, так как приложение публикуется доверенным издателем.

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**Редиректионварнингтипемакс** (0x0005)


</dt> <dd>

Диалоговое окно не отображается, так как приложение публикуется доверенным издателем.

</dd> </dl>

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Значение **редиректионварнингтипедефаулт**, которое является значением этого свойства по умолчанию, не оказывает никакого контроля над диалоговым окном. Свойство управления в данном случае — [**шовредиректионварнингдиалог**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) в [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





