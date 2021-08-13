---
description: Метод Енаблиффектс включает или отключает все эффекты на временной шкале. Если эффекты отключены, они остаются на временной шкале, но не подготавливаются к просмотру.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'Метод Иамтимелине:: Енаблиффектс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a6cce5d06b65bb6a7b3b6063e6cf6b9190e268ba7ee5f5abadf4343be2cf64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401115"
---
# <a name="iamtimelineenableeffects-method"></a>Метод Иамтимелине:: Енаблиффектс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`EnableEffects`Метод включает или отключает все эффекты на временной шкале. Если эффекты отключены, они остаются на временной шкале, но не подготавливаются к просмотру.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фенаблед* 
</dt> <dd>

Логическое значение, указывающее, следует ли включать или отключать эффекты. Если **значение равно true**, эффекты включены. Если задано **значение false**, эффекты отключены.

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелине**](iamtimeline.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




