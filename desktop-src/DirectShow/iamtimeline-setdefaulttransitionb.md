---
description: 'Метод Сетдефаулттранситионб задает переход по умолчанию. Этот метод эквивалентен Иамтимелине:: Сетдефаулттранситион, но принимает значение BSTR, а не указатель на GUID.'
ms.assetid: 1998fd31-2ab8-477e-89ee-93ca92dc10ec
title: 'Метод Иамтимелине:: Сетдефаулттранситионб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2a6ab2205c1d86c747ffcabbe69a88de8898fa1315ec98f9b816a5f5983dee59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905254"
---
# <a name="iamtimelinesetdefaulttransitionb-method"></a>Метод Иамтимелине:: Сетдефаулттранситионб

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetDefaultTransitionB`Метод задает переход по умолчанию. Этот метод эквивалентен [**иамтимелине:: сетдефаулттранситион**](iamtimeline-setdefaulttransition.md), но принимает значение BSTR, а не указатель на GUID.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDefaultTransitionB(
   BSTR pGuid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуид* 
</dt> <dd>

Значение BSTR, представляющее GUID перехода по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелине**](iamtimeline.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




