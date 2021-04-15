---
description: Метод Вритегрффиле записывает граф фильтра в файл в формате ГРФ.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'Метод IXml2Dex:: Вритегрффиле (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688883"
---
# <a name="ixml2dexwritegrffile-method"></a>Метод IXml2Dex:: Вритегрффиле

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`WriteGrfFile`Метод записывает граф фильтра в файл в формате ГРФ.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пграф* 
</dt> <dd>

Указатель на интерфейс **IUnknown** графа фильтра.

</dd> <dt>

*FileName* 
</dt> <dd>

Строка, указывающая имя файла для записи.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** , которое зависит от реализации интерфейса. HRESULT может содержать одну из следующих стандартных констант или другие значения, отсутствующие в списке.



| Код возврата                                                                                  | Описание                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**\_Ошибка E**</dt> </dl>       | Ошибка.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый аргумент.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>         | Успешно.<br/>             |



 

Этот метод также может возвращать коды ошибок, создаваемые внутренними вызовами методов **IStorage:: креатестреам** и **IPersist:: Save** . Дополнительные сведения см. в разделе пакет SDK для платформы.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Internet Explorer 4,0 или более поздней версии<br/>                                               |
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




