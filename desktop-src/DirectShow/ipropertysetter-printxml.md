---
description: Метод Принтксмл преобразует данные свойств в XML-строку.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: 'Ипропертисеттер: метод:P Ринтксмл (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675807"
---
# <a name="ipropertysetterprintxml-method"></a>Ипропертисеттер: метод:P Ринтксмл

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`PrintXML`Метод преобразует данные свойства в XML-строку.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзксмл* \[ заполняет\]
</dt> <dd>

Указатель на буфер, который получает XML-строку.

</dd> <dt>

*кбксмл* \[ окне\]
</dt> <dd>

Размер буфера, на который указывает *псзксмл*, в байтах.

</dd> <dt>

*пкбпринтед* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает длину XML-строки. Может иметь **значение NULL**.

</dd> <dt>

*Отступ* \[ окне\]
</dt> <dd>

Число уровней отступа для самого внешнего тега.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_При успешном выполнении возвращает значение ОК. В противном случае возвращает значение **HRESULT** , указывающее причину ошибки. Если строка XML длиннее, чем буфер, метод возвращает E \_ OUTOFMEMORY.

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

[**Интерфейс Ипропертисеттер**](ipropertysetter.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




