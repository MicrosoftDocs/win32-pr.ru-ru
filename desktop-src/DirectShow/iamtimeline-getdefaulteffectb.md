---
description: 'Метод Жетдефаултеффектб извлекает результат по умолчанию. Этот метод эквивалентен Иамтимелине:: Жетдефаултеффект, но получает значение BSTR, а не GUID.'
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: 'Метод Иамтимелине:: Жетдефаултеффектб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f0abfac297817b4e93b4eabe5bd2517c22ab363498bbbe35f2b5ae449524ecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997774"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a>Метод Иамтимелине:: Жетдефаултеффектб

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetDefaultEffectB`Метод получает результат по умолчанию. Этот метод эквивалентен [**иамтимелине:: жетдефаултеффект**](iamtimeline-getdefaulteffect.md), но получает значение **BSTR** , а не GUID.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуид* \[ out, retval\]
</dt> <dd>

Получает значение **BSTR** , ПРЕДСТАВЛЯЮЩЕЕ идентификатор GUID для действия по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Метод выделяет память для строки. Приложение должно вызвать **сисфристринг** для освобождения памяти.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелине**](iamtimeline.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




