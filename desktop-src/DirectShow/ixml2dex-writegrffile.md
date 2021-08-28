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
ms.openlocfilehash: 121d901bee9da9b8ea6f7dad31e589002c0b4859619f6dd02941f438af3b647f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767024"
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

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Internet Explorer 4,0 или более поздней версии<br/>                                               |
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




