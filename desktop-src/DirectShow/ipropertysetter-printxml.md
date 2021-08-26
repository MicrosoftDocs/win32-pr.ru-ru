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
ms.openlocfilehash: 5070a6906d7f30ab12171f551270f82b9851fa8c3990fade47aca6d2927509be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051514"
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

## <a name="remarks"></a>Remarks

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

[**Интерфейс Ипропертисеттер**](ipropertysetter.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




