---
description: Удаляет указанный исходный буфер из коллекции исходных буферов, управляемых объектом Имфмедиасаурцеекстенсион.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: 'Метод Имфмедиасаурцеекстенсион:: Ремовесаурцебуффер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2a093401058895f31b29843778a18a040e722c33
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351515"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a>Метод Имфмедиасаурцеекстенсион:: Ремовесаурцебуффер

Удаляет указанный исходный буфер из коллекции исходных буферов, управляемых объектом [**имфмедиасаурцеекстенсион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псаурцебуффер* \[ окне\]
</dt> <dd>

Буфер для удаления.

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

[**имфмедиасаурцеекстенсион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




