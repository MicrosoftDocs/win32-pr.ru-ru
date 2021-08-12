---
description: Открывает журнал графики.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипиксенгине:: OpenFile'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 35c448dc575eb5c85f7b3976e2e82f79aaa555f514ca8a433ba05fa4d1d21c61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283040"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>Метод Ипиксенгине:: OpenFile

Открывает журнал графики.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a>Параметры

*Файлов*   
Строка COM, содержащая имя журнала графики.

*регистрибут*   
Строка COM, содержащая корень реестра. Обработчик ищет DIA и другие разделы реестра.

*обратные вызовы*   
Адрес функции, используемой для уведомления узла о том, что были проанализированы новые кадры.

*пфилеиокаллбакк*   
Адрес функции, используемой для уведомления узла об ошибках ввода-вывода в файле во время синтаксического анализа.

*уилокале*   
КОД локали, используемый для отображения сообщений об ошибках в соответствии с настройками языкового стандарта.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ипиксенгине**](/windows/desktop/direct3dtools/ipixengine)

 

 
