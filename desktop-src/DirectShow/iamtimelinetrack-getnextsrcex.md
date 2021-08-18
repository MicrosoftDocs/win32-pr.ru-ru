---
description: Метод Жетнекстсрцекс извлекает следующий источник после указанного источника.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'Метод Иамтимелинетракк:: Жетнекстсрцекс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 438fcdbf4f95406994f5bf0cc63ebf5b5f600a9908419b63c4ceace65dfa9659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952803"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a>Метод Иамтимелинетракк:: Жетнекстсрцекс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetNextSrcEx`Метод извлекает следующий источник после указанного источника.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пласт* 
</dt> <dd>

Указатель на предыдущий исходный объект или **значение NULL** для получения первого источника в дорожке.

</dd> <dt>

*ппнекст* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) следующего исходного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК, если метод получает источник, или \_ false в противном случае.

## <a name="remarks"></a>Remarks

Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс **иамтимелинеобж** имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

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

[**Интерфейс Иамтимелинетракк**](iamtimelinetrack.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




