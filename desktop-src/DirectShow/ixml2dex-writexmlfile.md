---
description: Метод Вритексмлфиле преобразует временную шкалу в XML и записывает XML-данные в файл.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'Метод IXml2Dex:: Вритексмлфиле (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 81cb33222988b99b9484226e72110afc3eca1923441479adc8d600e2b80f273c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767014"
---
# <a name="ixml2dexwritexmlfile-method"></a>Метод IXml2Dex:: Вритексмлфиле

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`WriteXMLFile`Метод преобразует временную шкалу в XML и записывает XML-данные в файл.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птимелине* 
</dt> <dd>

Указатель на интерфейс **IUnknown** объекта временной шкалы.

</dd> <dt>

*FileName* 
</dt> <dd>

Строка, указывающая имя файла для записи.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** , которое зависит от реализации интерфейса. **HRESULT** может включать одну из следующих стандартных констант или другие значения, отсутствующие в списке.



| Код возврата                                                                                   | Описание                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый аргумент.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>             |



 

## <a name="remarks"></a>Remarks

Этот метод создает XML-файл, который представляет все компоненты на временной шкале.

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

 

 




