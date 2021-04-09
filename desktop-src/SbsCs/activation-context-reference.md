---
description: Контекстные функции и структуры активации используются с параллельными сборками.
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: Справочник по контексту активации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f8225b4db8b22227edf2b779ed9e1b50da7a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080753"
---
# <a name="activation-context-reference"></a>Справочник по контексту активации

Контекстные функции и структуры активации используются с параллельными сборками.

В следующей таблице перечислены функции контекста активации.



| Функция                                                   | Описание                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**активатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)                   | Активирует указанный контекст активации.                                                                                                             |
| [**аддрефакткткс**](/windows/desktop/api/Winbase/nf-winbase-addrefactctx)                       | Увеличивает значение счетчика ссылок указанного контекста активации.                                                                                     |
| [**креатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)                       | Создает контекст активации.                                                                                                                          |
| [**деактиватеакткткс**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx)               | Деактивирует указанный контекст активации.                                                                                                           |
| [**финдакткткссектионгуид**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | Возвращает данные, содержащиеся в структуре [**\_ \_ \_ данных раздела акткткс с ключом**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) , соответствующей указанному GUID.   |
| [**финдакткткссектионстринг**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | Возвращает данные, содержащиеся в структуре [**\_ \_ \_ данных раздела акткткс с ключом**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) , соответствующей указанной строке. |
| [**жеткуррентакткткс**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | Возвращает текущий контекст активации.                                                                                                                 |
| [**исолатионавареклеануп**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | Гарантирует освобождение памяти при загрузке, выгрузке и перезагрузке манифеста.                                                                         |
| [**куеряктктксв**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | Запрашивает в контексте активации сведения о сборке или файле.                                                                               |
| [**куерякткткссеттингсв**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | Указывает пространство имен и имя атрибута для запрашиваемого атрибута.                                                                      |
| [**релеасеакткткс**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | Уменьшает значение счетчика ссылок указанного контекста активации.                                                                                     |
| [**зомбифякткткс**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | Деактивирует указанный контекст активации, но не освобождает его.                                                                               |



 

В следующей таблице перечислены структуры контекста активации.



| Структура                                                                                                        | Описание                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ подробные \_ сведения о сборке контекста активации**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | Содержит подробные сведения о контексте активации.                                                                                                                                                                                                                                                                                                                                  |
| [**\_ \_ подробные \_ сведения о контексте активации**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | Содержит сведения о сборке в контексте активации.                                                                                                                                                                                                                                                                                                                           |
| [**\_ \_ индекс запроса контекста \_ активации**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | Содержит сборку в контексте активации и индекс файла в сборке.                                                                                                                                                                                                                                                                                           |
| [**акткткс**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | Содержит сведения, описывающие конкретный контекст активации.                                                                                                                                                                                                                                                                                                                           |
| [**\_данные раздела с \_ ключом \_ акткткс**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | Возвращает сведения о контексте активации, а также GUID или 32-разрядный раздел контекста активации с пометкой целых чисел.                                                                                                                                                                                                                                                                   |
| [**\_ \_ подробные \_ сведения о файле сборки**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | Содержит сведения о файле сборки в контексте активации.                                                                                                                                                                                                                                                                                                                 |
| [**\_ \_ \_ сведения об уровне выполнения контекста активации \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | Используется функцией [**куеряктктксв**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) .<br/> **Windows Server 2003 и Windows XP:** Эта структура недоступна.<br/>                                                                                                                                                                                                                                    |
| [**\_элемент контекста \_ совместимости**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | Используется функцией [**куеряктктксв**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) как часть структуры [**\_ \_ \_ сведений о совместимости контекста активации**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) . <br/> **Windows Server 2008 и более ранних версий, Windows Vista и более ранних версий:** Эта структура недоступна. Она доступна начиная с Windows Server 2008 R2 и Windows 7.<br/> |
| [**\_ \_ сведения о СОВМЕСТИМОСТИ контекста активации \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | Используется функцией [**куеряктктксв**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) .<br/> **Windows Server 2008 и более ранних версий, Windows Vista и более ранних версий:** Эта структура недоступна. Она доступна начиная с Windows Server 2008 R2 и Windows 7.<br/>                                                                                                                                   |



 

В следующей таблице перечислены перечисления контекста активации.

| Перечисление                                                                       | Описание                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**АКТКТКС \_ запрошенный \_ \_ уровень выполнения**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | Описывает запрошенный уровень выполнения контекста активации. **Windows Server 2003 и Windows XP:** Это перечисление недоступно.<br/>                                                                                                      |
| [**\_ \_ тип элемента совместимости \_ акткткс**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | Описывает элемент Compatibility в манифесте приложения. **Windows Server 2008 и более ранних версий, Windows Vista и более ранних версий:** Это перечисление недоступно. Она доступна начиная с Windows Server 2008 R2 и Windows 7.<br/> |



 

 

