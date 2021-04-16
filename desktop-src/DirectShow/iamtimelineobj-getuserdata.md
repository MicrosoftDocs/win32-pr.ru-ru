---
description: Метод UserData извлекает определяемые приложением постоянные данные.
ms.assetid: dd2cdb37-9c4f-4356-a35f-2d42b7588da6
title: 'Метод Иамтимелинеобж:: UserData (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9dda74980dcdae9cd73e749d9cb4324b4c6357f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679719"
---
# <a name="iamtimelineobjgetuserdata-method"></a>Метод Иамтимелинеобж:: UserData

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetUserData`Метод получает определяемые приложением постоянные данные.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetUserData(
   BYTE *pData,
   long *pSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* 
</dt> <dd>

Указатель на буфер, который получает данные. Чтобы определить размер выделяемого буфера, присвойте этому параметру **значение NULL**. Требуемый размер возвращается в *псизе*.

</dd> <dt>

*псизе* 
</dt> <dd>

Получает размер данных в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

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

[**Интерфейс Иамтимелинеобж**](iamtimelineobj.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




