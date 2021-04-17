---
description: 'Метод Жетдефаулттранситионб извлекает переход по умолчанию. Этот метод эквивалентен Иамтимелине:: Жетдефаулттранситион, но получает значение BSTR, а не GUID.'
ms.assetid: ed743766-e970-4bd9-a9a0-8b5d9fec2d80
title: 'Метод Иамтимелине:: Жетдефаулттранситионб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f150ca0fafff6b250776a38b7ec68beb470e9d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679870"
---
# <a name="iamtimelinegetdefaulttransitionb-method"></a>Метод Иамтимелине:: Жетдефаулттранситионб

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetDefaultTransitionB`Метод получает переход по умолчанию. Этот метод эквивалентен [**иамтимелине:: жетдефаулттранситион**](iamtimeline-getdefaulttransition.md), но получает значение BSTR, а не GUID.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDefaultTransitionB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуид* \[ out, retval\]
</dt> <dd>

Получает значение **BSTR** , ПРЕДСТАВЛЯЮЩЕЕ идентификатор GUID перехода по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Метод выделяет память для строки. Приложение должно вызвать **сисфристринг** для освобождения памяти.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелине**](iamtimeline.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




