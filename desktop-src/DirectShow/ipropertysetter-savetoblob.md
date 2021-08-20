---
description: Метод Саветоблоб сохраняет данные свойств в формате сохраняемости.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'Метод Ипропертисеттер:: Саветоблоб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c94cbb7b927e4bce7309e3e8a016b0e43bc6a0f9f3f319ee733e6e22132b47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952545"
---
# <a name="ipropertysettersavetoblob-method"></a>Метод Ипропертисеттер:: Саветоблоб

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SaveToBlob`Метод сохраняет данные свойства в формате сохраняемости.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пксизе* \[ заполняет\]
</dt> <dd>

Получает размер данных в байтах.

</dd> <dt>

*ППБ* \[ заполняет\]
</dt> <dd>

Получает указатель на массив байтов, который получает данные.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Метод выделяет память для массива байтов. Вызывающий объект должен освободить его с помощью функции **CoTaskMemFree** .

Все имена и значения свойств усекаются до 40 символов. По этой причине XML является предпочтительным форматом сохраняемости. См. раздел [**интерфейс IXml2Dex**](ixml2dex.md).

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

[**Интерфейс Ипропертисеттер**](ipropertysetter.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




