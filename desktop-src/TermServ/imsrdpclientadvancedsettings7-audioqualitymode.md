---
title: IMsRdpClientAdvancedSettings7 Аудиокуалитимоде, свойство
description: Указывает или получает значение, указывающее параметр режима качества звука для перенаправленного звука. По умолчанию установлено значение 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Аудиокуалитимоде
- Службы удаленных рабочих столов свойства Аудиокуалитимоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Аудиокуалитимоде
- Службы удаленных рабочих столов свойства Аудиокуалитимоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Аудиокуалитимоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681938"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a>Свойство IMsRdpClientAdvancedSettings7:: Аудиокуалитимоде

Указывает или получает значение, указывающее параметр режима качества звука для перенаправленного звука. По умолчанию установлено значение 0.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a>Значение свойства

Значение типа, указывающее режим качества звука.

Допустимые значения:

<dt>

0
</dt> <dd>

Динамическое качество звука. Это параметр качества звука по умолчанию. Сервер динамически корректирует качество вывода звука в ответ на условия сети и возможности клиента и сервера.

</dd> <dt>

1
</dt> <dd>

Средний качество звука. Сервер использует фиксированный, но сжатый формат для вывода звука.

</dd> <dt>

2
</dt> <dd>

Высокое качество звука. Сервер предоставляет выходные данные в несжатом формате PCM с меньшими затратами на обработку для задержки.

</dd> </dl>

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

 

 





