---
title: Тип конфиденциальности (WinInet. h)
description: Указывает, что параметры конфиденциальности предназначены для файлов cookie первого или сторонних поставщиков.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6f29461f57a2209fde00b30bce7914c207958f27e28062e2c3bd3d94d442e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743731"
---
# <a name="privacy-type"></a>Тип конфиденциальности

Указывает, что параметры конфиденциальности предназначены для файлов cookie первого или сторонних поставщиков.

<dl> <dt>

<span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**\_тип конфиденциальности \_ First \_ вечеринка**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Относится к параметрам конфиденциальности для файлов cookie первого производителя.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**\_тип конфиденциальности \_ третья \_ сторона**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Относится к параметрам конфиденциальности для файлов cookie сторонних производителей.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Файлы cookie классифицируются как первая сторона и третья сторона. Первичный файл cookie — это тот, который поступает из домена узла. Если https://www.blueyonderairlines.com в адресной строке Microsoft Internet Explorer обнаружено значение "", то "www.blueyonderairlines.com" является доменом узла. При посещении этой страницы, если файл cookie задан из домена, отличного от "www.blueyonderairlines.com", например "www.fourthcoffee.com", этот файл cookie считается сторонним файлом cookie.

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**привацижетзонепреференцев**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**привацисетзонепреференцев**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

