---
description: Метод Реадксмлфиле загружает файл XML-проекта.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'Метод IXml2Dex:: Реадксмлфиле (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689338"
---
# <a name="ixml2dexreadxmlfile-method"></a>Метод IXml2Dex:: Реадксмлфиле

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`ReadXMLFile`Метод загружает файл XML-проекта. Этот метод создает экземпляры всех объектов, выраженные в XML-файле и вставляет их на временную шкалу, а также применяет любые атрибуты, заданные для временной шкалы, такие как частота кадров или эффекты по умолчанию.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птимелине* 
</dt> <dd>

Указатель на интерфейс **IUnknown** объекта временной шкалы.

</dd> <dt>

*XMLName* 
</dt> <dd>

Строка, указывающая имя загружаемого файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение HRESULT. Ниже приведены возможные значения.



| Код возврата                                                                                                  | Описание                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                         | Успешно<br/>             |
| <dl> <dt>**\_ \_ Недопустимый \_ Формат файла VFW E \_**</dt> </dl> | Недопустимый формат файла<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод не удаляет существующие объекты с временной шкалы перед вставкой новых объектов, определенных в XML-файле. Если необходимо обновить существующую временную шкалу, сначала вызовите метод [**иамтимелине:: клеараллграупс**](iamtimeline-clearallgroups.md) .

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

 

 




