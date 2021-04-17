---
description: Метод метода Timeline извлекает временную шкалу, к которой принадлежит эта группа.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: Метод Иамтимелинеграуп::-Timeline (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b85b0c6f1730c2946134a36d33537f311b6603f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675618"
---
# <a name="iamtimelinegroupgettimeline-method"></a>Метод Иамтимелинеграуп:: with Timeline

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetTimeline`Метод извлекает временную шкалу, к которой принадлежит эта группа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пптимелине* \[ заполняет\]
</dt> <dd>

Получает интерфейс [**иамтимелине**](iamtimeline.md) временной шкалы. Если группа не является частью временной шкалы, для нее устанавливается значение **null**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Если значение, возвращаемое в *пптимелине* , не равно **null**, то интерфейс **иамтимелине** имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

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

[**Интерфейс Иамтимелинеграуп**](iamtimelinegroup.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




