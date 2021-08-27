---
description: Предоставляет сведения для методов интерфейса ИкуеряссоЦиатионс.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Перечисление АССОКФ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d52de3ce181033358fc20ca3e4f8759b61f72ed
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786700"
---
# <a name="assocf-enumeration"></a>Перечисление АССОКФ

Предоставляет сведения для методов интерфейса [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .

## <a name="syntax"></a>Синтаксис




| C++ | 
|-----|
| <pre><code>typedef enum  {   ASSOCF_NONE                  = 0x00000000,  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,  ASSOCF_INIT_BYEXENAME        = 0x00000002,  ASSOCF_OPEN_BYEXENAME        = 0x00000002,  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,  ASSOCF_NOUSERSETTINGS        = 0x00000010,  ASSOCF_NOTRUNCATE            = 0x00000020,  ASSOCF_VERIFY                = 0x00000040,  ASSOCF_REMAPRUNDLL           = 0x00000080,  ASSOCF_NOFIXUPS              = 0x00000100,  ASSOCF_IGNOREBASECLASS       = 0x00000200,  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,  ASSOCF_IS_PROTOCOL           = 0x00001000,  ASSOCF_INIT_FOR_FILE         = 0x00002000} ASSOCF;</code></pre> | 




## <a name="constants"></a>Константы

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**АССОКФ \_ None** 

Не задан ни один из следующих параметров.

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**АССОКФ \_ init \_ норемапклсид** 

Указывает, что методы интерфейса [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) не СОПОСТАВЛЯЮТ значения CLSID со значениями ProgID.

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**АССОКФ \_ init \_ бексенаме** 

Определяет значение параметра *Пвсзассок* [**ИкуеряссоЦиатионс:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) в качестве имени исполняемого файла. Если этот флаг не установлен, для корневого ключа будет задан идентификатор ProgID, связанный с ключом **.exe** , а не ProgID исполняемого файла.

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**АССОКФ \_ Open \_ бексенаме** 

Идентично **ассокф \_ init \_ бексенаме**.

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**АССОКФ \_ init \_ дефаулттостар** 

Указывает, что когда метод [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) не находит запрошенное значение в корневом ключе, он должен попытаться получить сравниваемое значение из **\*** подраздела.

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**АССОКФ \_ init \_ дефаулттофолдер** 

Указывает, что когда метод [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) не находит запрошенное значение в корневом ключе, он должен попытаться получить сравниваемое значение из подраздела **Folder** .

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**АССОКФ \_ наусерсеттингс** 

Указывает, что должен быть выполнен поиск только **\_ \_ корневых классов hKey** , и **\_ текущий \_ пользователь hKey** должен игнорироваться.

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**АССОКФ \_ усечение** 

Указывает, что возвращаемая строка не должна быть усечена. Вместо этого следует возвращать значение ошибки и необходимый размер для полной строки.

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**\_Проверка ассокф** 

Инструктирует методы [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) для проверки правильности данных. Этот параметр позволяет методам **икуеряссоЦиатионс** считывать данные с жесткого диска пользователя для проверки. Например, они могут проверить понятное имя в реестре на соответствие сохраненному в файле .exe. Установка этого флага обычно сокращает эффективность метода.

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**АССОКФ \_ ремапрундлл** 

Указывает, что методы [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) не пропускают Rundll.exe и возвращают сведения о ее целевом объекте. Обычно методы **икуеряссоЦиатионс** возвращают сведения о первом .exe или .dll в командной строке. Если команда использует Rundll.exe, установка этого флага указывает методу игнорировать Rundll.exe и возвращать сведения о целевом объекте.

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**АССОКФные \_ исправления** 

Указывает методам [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) не исправлять ошибки в реестре, например понятное имя функции, не совпадающее с именем, найденным в файле .exe.

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**АССОКФ \_ игноребасекласс** 

Указывает, что значение BaseClass следует игнорировать.

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**АССОКФ \_ init \_ игнореункновн** 

**появилось в Windows 7**. Указывает, что ProgID "Unknown" следует игнорировать. Вместо этого происходит сбой.

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**\_ \_ фиксированный \_ идентификатор ProgID ассокф init** 

**Введено в Windows 8**. Указывает, что указанный идентификатор ProgID должен быть сопоставлен с использованием системных значений по умолчанию, а не по умолчанию текущего пользователя.

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**АССОКФ \_ — \_ протокол** 

**Введено в Windows 8**. Указывает, что значение является протоколом и должно быть сопоставлено с текущими значениями по умолчанию для текущего пользователя.

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**\_Инициализация ассокф \_ для \_ файла** 

**Введено в Windows 8.1**. Указывает, что идентификатор ProgID соответствует сопоставлению на основе расширения файла. Используйте совместно с **\_ \_ фиксированным \_ идентификатором ProgID ассокф init**.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]               |
| Минимальная версия сервера | Windows 2000 Server \[только классические приложения\]                                 |
| Заголовок                   |  Shlwapi. h  |



## <a name="see-also"></a>См. также

 [**Ассоккуерикэй**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**ассоккуеристринг**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**ассоккуеристрингбикэй**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© Майкрософт (Microsoft), 2017. Все права защищены.
