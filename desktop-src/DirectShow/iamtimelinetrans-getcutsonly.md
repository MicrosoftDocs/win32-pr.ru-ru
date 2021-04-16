---
description: Метод Жеткутсонли определяет, визуализируется ли переход в виде вырезания. Если да, то переход выполняется мгновенно в вырезанной точке.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'Метод Иамтимелинетранс:: Жеткутсонли (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689447"
---
# <a name="iamtimelinetransgetcutsonly-method"></a>Метод Иамтимелинетранс:: Жеткутсонли

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetCutsOnly`Метод определяет, визуализируется ли переход в виде вырезания. Если да, то переход выполняется мгновенно в вырезанной точке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pVal* 
</dt> <dd>

Получает логическое значение, указывающее, визуализируется ли переход в виде вырезания. Если **значение равно true**, то переход является мгновенно вырезанным. Если **значение равно false**, переход выполняется в течение нормальной длительности.

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

[**Интерфейс Иамтимелинетранс**](iamtimelinetrans.md)
</dt> <dt>

[**Иамтимелинетранс:: Сеткутсонли**](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[**Иамтимелинетранс:: Жеткутпоинт**](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[**Иамтимелине:: Транситионсенаблед**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




