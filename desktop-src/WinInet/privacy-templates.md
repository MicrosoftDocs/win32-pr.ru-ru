---
title: Шаблоны конфиденциальности (WinInet. h)
description: Ниже приведены уровни конфиденциальности, которые соответствуют правилам принятия, условного принятия или отсутствия приема файлов cookie.
ms.assetid: d8dd9c12-b159-4f95-820e-521aeb1526bf
topic_type:
- apiref
api_name:
- PRIVACY_TEMPLATE_NO_COOKIES
- PRIVACY_TEMPLATE_HIGH
- PRIVACY_TEMPLATE_MEDIUM_HIGH
- PRIVACY_TEMPLATE_MEDIUM
- PRIVACY_TEMPLATE_MEDIUM_LOW
- PRIVACY_TEMPLATE_LOW
- PRIVACY_TEMPLATE_CUSTOM
- PRIVACY_TEMPLATE_ADVANCED
- PRIVACY_TEMPLATE_MAX
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481aa3e9b6b5b5519bac6e458de1acba90f2cfa20dd0a5babac016d0003c70b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955564"
---
# <a name="privacy-templates"></a>Шаблоны конфиденциальности

Ниже приведены уровни конфиденциальности, которые соответствуют правилам принятия, условного принятия или отсутствия приема файлов cookie. Эти уровни соответствуют уровням предпочтений конфиденциальности, заданным на вкладке Конфиденциальность в свойствах обозревателя. Подробные определения см. [в разделе о конфиденциальности в Internet Explorer 6](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) .

<dl> <dt>

<span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**\_шаблон конфиденциальности \_ без \_ файлов cookie**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Это аналогично **блокировке всех файлов cookie** на ползунке настройки конфиденциальности в **свойствах браузера**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**\_шаблон конфиденциальности \_ высокий**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Это то **же самое, что и** ползунок «настройки конфиденциальности» в окне « **Свойства обозревателя**».


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**\_шаблон конфиденциальности \_ среднего \_ высокого уровня**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Это то **же самое, что \_ и** на ползунке настройки конфиденциальности в **свойствах обозревателя**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**\_ \_ средний уровень шаблона конфиденциальности**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Это аналогично **среднему** значению ползунка настройки конфиденциальности в **свойствах обозревателя**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**\_шаблон конфиденциальности \_ Medium \_ низкий** 
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Это то же самое, **что и** ползунок «настройки конфиденциальности» в окне « **Свойства обозревателя**».


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**\_шаблон конфиденциальности \_ низкий**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Это то же самое, что и « **принимать все файлы cookie** » ползунка «параметры конфиденциальности» в окне « **Свойства обозревателя**».


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**\_Пользовательский шаблон \_ конфиденциальности**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Определяется пользователем. Сведения о настройке пользовательских параметров конфиденциальности см. в разделе [Создание пользовательского файла импорта данных о конфиденциальности](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) .


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**\_Расширенный шаблон \_ конфиденциальности**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Определяется пользователем. дополнительные параметры задаются в диалоговом окне **расширенная Параметры о конфиденциальности** , доступном на вкладке **конфиденциальность** диалогового окна **свойства обозревателя**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**\_ \_ максимальный размер шаблона конфиденциальности**
</dt> <dd> <dl> <dt>

\_шаблон конфиденциальности \_ низкий
</dt> <dt>



То же, что и **\_ шаблон конфиденциальности \_ низкая**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**привацижетзонепреференцев**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**привацисетзонепреференцев**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

