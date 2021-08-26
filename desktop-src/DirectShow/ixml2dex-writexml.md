---
description: Метод WriteXML преобразует временную шкалу в XML-строку.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'Метод IXml2Dex:: WriteXML (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a5285faad36f83dbab693c63a0c96ca2b1d2b6a25220bb601a9527aac9dc5ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051294"
---
# <a name="ixml2dexwritexml-method"></a>Метод IXml2Dex:: WriteXML

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`WriteXML`Метод преобразует временную шкалу в XML-строку.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птимелине* 
</dt> <dd>

Указатель на интерфейс **IUnknown** объекта временной шкалы.

</dd> <dt>

*пбстрксмл* 
</dt> <dd>

Указатель на переменную типа BSTR, которая получает XML-строку, описывающую временную шкалу.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_При успешном выполнении возвращает значение ОК. При нехватке памяти для преобразования возвращает E \_ OUTOFMEMORY. В противном случае возвращает другой код ошибки.

## <a name="remarks"></a>Remarks

Метод выделяет память для строки. Приложение должно вызвать **сисфристринг** для освобождения памяти.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Internet Explorer 4,0 или более поздней версии<br/>                                               |
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




