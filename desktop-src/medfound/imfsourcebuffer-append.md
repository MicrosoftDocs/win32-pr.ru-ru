---
description: Добавляет указанный сегмент мультимедиа в Имфсаурцебуффер.
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
title: 'Метод Имфсаурцебуффер:: Append'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Append
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 00c9b6a0af2e48482311a8a0e1bc39dc4ce951aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263369"
---
# <a name="imfsourcebufferappend-method"></a>Метод Имфсаурцебуффер:: Append

Добавляет указанный сегмент мультимедиа в [**имфсаурцебуффер**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Append(
  [in] const BYTE  *pData,
  [in]       DWORD len
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ окне\]
</dt> <dd>

Добавляемые данные мультимедиа.

</dd> <dt>

*Len* \[ окне\]
</dt> <dd>

Длина данных мультимедиа, хранящихся в *pData*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфсаурцебуффер**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




