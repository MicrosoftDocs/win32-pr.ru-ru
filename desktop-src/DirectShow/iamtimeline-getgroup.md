---
description: Метод-Group извлекает указанную группу.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: Метод Иамтимелине::-Group (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71bf4aa0dd5d6f338da43d71384ead024fe821d3a639b0021299f6f6deb14be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685194"
---
# <a name="iamtimelinegetgroup-method"></a>Метод Иамтимелине:: Group

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetGroup`Метод извлекает указанную группу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппграуп* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) группы.

</dd> <dt>

*вхичграуп* 
</dt> <dd>

Индекс извлекаемой группы в зависимости от порядка добавления групп на временную шкалу. Первая группа, добавленная на временную шкалу, имеет индекс 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Если метод завершается успешно, интерфейс **иамтимелинеобж** , который он возвращает, имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

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

 

 




