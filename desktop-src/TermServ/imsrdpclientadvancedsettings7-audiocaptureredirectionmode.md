---
title: IMsRdpClientAdvancedSettings7 Аудиокаптурередиректионмоде, свойство
description: Указывает или получает логическое значение, указывающее, перенаправляется ли устройство ввода звука по умолчанию с клиента на удаленный сеанс.
ms.assetid: e75add5e-4652-41a7-b2cb-2c60793cd079
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Аудиокаптурередиректионмоде
- Службы удаленных рабочих столов свойства Аудиокаптурередиректионмоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Аудиокаптурередиректионмоде
- Службы удаленных рабочих столов свойства Аудиокаптурередиректионмоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Аудиокаптурередиректионмоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioCaptureRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be6083a3b609a558830b9e7b837acce179ac7a098315b2bfeeacca800bfdc85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138797"
---
# <a name="imsrdpclientadvancedsettings7audiocaptureredirectionmode-property"></a>Свойство IMsRdpClientAdvancedSettings7:: Аудиокаптурередиректионмоде

Указывает или получает логическое значение, указывающее, перенаправляется ли устройство ввода звука по умолчанию с клиента на удаленный сеанс.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_AudioCaptureRedirectionMode(
  [in]          VARIANT_BOOL fRedir
);

HRESULT get_AudioCaptureRedirectionMode(
  [out, retval] VARIANT_BOOL *pfRedir
);
```



## <a name="property-value"></a>Значение свойства

Значение **типа \_ Variant** , указывающее, перенаправляется ли запись звука. Укажите **вариант \_ true** , если хотите перенаправлять запись звука.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





