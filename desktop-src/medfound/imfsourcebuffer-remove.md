---
description: Удаляет сегменты носителя, определенные в указанном диапазоне времени, из Имфсаурцебуффер.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: 'Метод Имфсаурцебуффер:: Remove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: af9aed011a1a4b53733d70646fc14b21e7c97f9d193a60e679f5f5f532679e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941914"
---
# <a name="imfsourcebufferremove-method"></a>Метод Имфсаурцебуффер:: Remove

Удаляет сегменты носителя, определенные в указанном диапазоне времени, из [**имфсаурцебуффер**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Запуск* \[ окне\]
</dt> <dd>

Начало диапазона времени.

</dd> <dt>

*конец* \[ окне\]
</dt> <dd>

Конец диапазона времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имфсаурцебуффер**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




