---
description: в этом разделе описываются функции обработки реестра оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.
title: Функции обработки реестра оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 12182f56-5bb3-4f70-ae6a-2ef7366287b9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7bd7204ada31db6791d3cb78d1a11087d19eae45f0cacbfdf6ae6e032ae66a04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676503"
---
# <a name="shell-registry-handling-functions"></a>Функции обработки реестра оболочки

в этом разделе описываются функции обработки реестра оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                             | Описание                                                                                                                                                                         |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ассоккреате**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate)<br/>                     | Возвращает указатель на объект [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .<br/>                                                                                         |
| [**ассокжетперцеиведтипе**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)<br/> | Извлекает воспринимаемый тип файла на основе его расширения.<br/>                                                                                                                |
| [**ассоЦисданжераус**](/windows/desktop/api/Shlwapi/nf-shlwapi-associsdangerous)<br/>           | Определяет, считается ли тип файла потенциальной угрозой безопасности.<br/>                                                                                                  |
| [**ассоккуерикэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerykeya)<br/>                 | Выполняет поиск и извлекает ключ, связанный с сопоставлением файлов или протоколов, из реестра.<br/>                                                                            |
| [**ассоккуеристринг**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)<br/>           | Выполняет поиск и извлекает из реестра строку, связанную с сопоставлением файлов или протоколов.<br/>                                                                              |
| [**ассоккуеристрингбикэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringbykeya)<br/> | Ищет и извлекает строку, связанную с сопоставлением файлов, из реестра, начиная с указанного ключа.<br/>                                                            |
| [**шкопикэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya)<br/>                         | Рекурсивно копирует подразделы и значения исходного подраздела в целевой раздел. [**Шкопикэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya) не копирует атрибуты безопасности ключей.<br/> |
| [**шделетимптикэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeleteemptykeya)<br/>           | Удаляет пустой ключ.<br/>                                                                                                                                                    |
| [**шделетекэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletekeya)<br/>                     | Удаляет подраздел и все его потомки. Эта функция удаляет ключ и все значения ключа из реестра.<br/>                                                      |
| [**шделетевалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletevaluea)<br/>                 | Удаляет именованное значение из указанного раздела реестра.<br/>                                                                                                                   |
| [**шенумкэйекс**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumkeyexa)<br/>                     | Перечисляет подразделы указанного открытого раздела реестра.<br/>                                                                                                               |
| [**шенумвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumvaluea)<br/>                     | Перечисляет значения указанного открытого ключа реестра.<br/>                                                                                                                |
| [**шжетассоккэйс**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetassockeys)<br/>               | Извлекает массив подразделов класса, связанных с объектом [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .<br/>                                                          |
| [**шжетвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetvaluea)<br/>                       | Извлекает значение реестра.<br/>                                                                                                                                              |
| [**SHOpenRegStream2**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a)<br/>           | Открывает значение реестра и предоставляет поток, который можно использовать для чтения или записи значения. Эта функция заменяет [**шопенрегстреам**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama).<br/>   |
| [**шкуеринфокэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryinfokeya)<br/>               | Извлекает сведения об указанном разделе реестра.<br/>                                                                                                                    |
| [**шкуеривалуикс**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryvalueexa)<br/>               | Открывает раздел реестра и запрашивает его для определенного значения.<br/>                                                                                                                |
| [**шрегклосеускэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcloseuskey)<br/>             | Закрывает маркер для конкретного пользователя в поддереве пользователя (HKEY \_ текущий \_ пользователь или раздел hKey \_ \_ ).<br/>                                             |
| [**шрегкреатеускэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcreateuskeya)<br/>           | Создание или открытие подраздела реестра в поддереве пользователя (HKEY \_ текущий \_ пользователь или hKey \_ локальный \_ компьютер).<br/>                                                             |
| [**шрегделетимптюскэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteemptyuskeya)<br/> | Удаляет пустой подраздел реестра в поддереве конкретного пользователя (HKEY \_ текущий \_ пользователь или раздел hKey \_ \_ ).<br/>                                                               |
| [**шрегделетеусвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteusvaluea)<br/>       | Удаляет значение подраздела реестра в поддереве пользователя (HKEY \_ текущий \_ пользователь или hKey \_ локальный \_ компьютер).<br/>                                                                |
| [**шрегдупликатехкэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregduplicatehkey)<br/>       | Дублирует маркер HKEY раздела реестра.<br/>                                                                                                                                 |
| [**шреженумускэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumuskeya)<br/>               | Перечисляет подразделы подраздела реестра в поддереве пользователя (HKEY \_ текущий \_ пользователь или hKey \_ локальный \_ компьютер).<br/>                                                    |
| [**шреженумусвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumusvaluea)<br/>           | Перечисление значений указанного подраздела реестра в поддереве пользователя (HKEY \_ текущий \_ пользователь или hKey \_ локальный \_ компьютер).<br/>                                         |
| [**шрегжетбулусвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetboolusvaluea)<br/>     | Извлекает логическое значение из подраздела реестра для конкретного пользователя поддерева (HKEY \_ текущий \_ пользователь или hKey \_ локальный \_ компьютер).<br/>                                               |
| [**шрегжетинтв**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetintw)<br/>                    | Считывает числовое строковое значение из реестра и преобразует его в целое число.<br/>                                                                                            |
| [**шрегжетпас**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetpatha)<br/>                   | Извлекает путь к файлу из реестра, расширяя переменные среды по мере необходимости.<br/>                                                                                      |
| [**шрегжетусвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetusvaluea)<br/>             | Извлекает значение из подраздела реестра для конкретного пользователя поддерева (HKEY \_ текущий \_ пользователь или hKey \_ локальный \_ компьютер).<br/>                                                       |
| [**шрегопенускэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregopenuskeya)<br/>               | Открывает подраздел реестра в поддереве пользователя (HKEY \_ текущий \_ пользователь или hKey \_ локальный \_ компьютер).<br/>                                                                        |
| [**шрегкуеринфаускэй**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryinfouskeya)<br/>     | Извлекает сведения об указанном подразделе реестра в поддереве пользователя (HKEY \_ Current \_ User или hKey \_ Local \_ Machine).<br/>                                        |
| [**шрегкуерюсвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryusvaluea)<br/>         | Извлекает тип и данные для указанного имени, связанного с открывающим подразделом реестра в поддереве пользователя (HKEY \_ Current \_ User или hKey \_ Local \_ Machine).<br/>       |
| [**шрегсетпас**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetpatha)<br/>                   | Принимает путь к файлу, заменяет имена папок строками среды и помещает результирующую строку в реестр.<br/>                                                      |
| [**шрегсетусвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetusvaluea)<br/>             | Задает значение подраздела реестра в поддереве пользователя (HKEY \_ текущий \_ пользователь или hKey \_ локальный \_ компьютер).<br/>                                                                   |
| [**шрегсетвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)<br/>                 | Задает значение реестра.<br/> Используйте [**регсетвалуе**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) на своем месте.<br/>                                                                                  |
| [**шрегвритеусвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregwriteusvaluea)<br/>         | Записывает значение в подраздел реестра в поддереве для конкретного пользователя (HKEY \_ текущий \_ пользователь или hKey \_ локальный \_ компьютер).<br/>                                                            |
| [**шсетвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetvaluea)<br/>                       | Задает значение раздела реестра.<br/>                                                                                                                                        |



 

 

 
