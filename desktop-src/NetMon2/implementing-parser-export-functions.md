---
description: Функции экспорта средства синтаксического анализа предоставляют все функциональные возможности средств синтаксического анализа в библиотеке DLL средства синтаксического анализа. Каждая библиотека DLL анализатора должна реализовывать Парсераутоинсталлинфо и DllMain. Оставшиеся функции экспорта должны быть реализованы для каждого средства синтаксического анализа, входящего в библиотеку DLL средства синтаксического анализа.
ms.assetid: be73623c-7ae7-4ca9-be6c-52f513cd38a4
title: Реализация функций экспорта средства синтаксического анализа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b8eafb7e12c36a9413a320652e3d372ffbf51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540170"
---
# <a name="implementing-parser-export-functions"></a>Реализация функций экспорта средства синтаксического анализа

Функции экспорта средства синтаксического анализа предоставляют все функциональные возможности средств синтаксического анализа в библиотеке DLL средства синтаксического анализа. Каждая библиотека DLL анализатора должна реализовывать [**парсераутоинсталлинфо**](parserautoinstallinfo.md) и [**DllMain**](dllmain-parser.md). Оставшиеся функции экспорта должны быть реализованы для каждого средства синтаксического анализа, входящего в библиотеку DLL средства синтаксического анализа.

В следующих разделах показано, как реализовать функции экспорта.



| Термин                                                                                                                                                                                                                                                   | Описание                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Implementing_ParserAutoInstallInfo"></span><span id="implementing_parserautoinstallinfo"></span><span id="IMPLEMENTING_PARSERAUTOINSTALLINFO"></span>[Реализация Парсераутоинсталлинфо](implementing-parserautoinstallinfo.md)<br/> | Содержит описание и пример кода реализации функции [**парсераутоинсталлинфо**](parserautoinstallinfo.md) , которая определяет средства синтаксического анализа, расположенные в библиотеке DLL средства синтаксического анализа.<br/>                                                                                            |
| <span id="Implementing_DllMain_Parser"></span><span id="implementing_dllmain_parser"></span><span id="IMPLEMENTING_DLLMAIN_PARSER"></span>[Реализация средства синтаксического анализа DllMain](implementing-dllmain-parser.md)<br/>                                    | Содержит описание и пример кода реализации функции [**синтаксического анализа DllMain**](dllmain-parser.md) , которая определяет существование средства синтаксического анализа, а затем освобождает ресурсы, которые сетевой монитор использует для анализатора.<br/>                                              |
| <span id="Implementing_Register"></span><span id="implementing_register"></span><span id="IMPLEMENTING_REGISTER"></span>[Реализация регистра](implementing-register.md)<br/>                                                                  | Содержит описание и пример кода реализации функции [**Register**](register-parser.md) , которая записывает все свойства протокола.<br/>                                                                                                                     |
| <span id="Implementing_RecognizeFrame"></span><span id="implementing_recognizeframe"></span><span id="IMPLEMENTING_RECOGNIZEFRAME"></span>[Реализация Рекогнизефраме](implementing-recognizeframe.md)<br/>                                    | Содержит описание и пример кода реализации функции [**рекогнизефраме**](recognizeframe.md) , которая определяет экземпляр протокола в кадре.<br/>                                                                                                         |
| <span id="Implementing_AttachProperties"></span><span id="implementing_attachproperties"></span><span id="IMPLEMENTING_ATTACHPROPERTIES"></span>[Реализация Аттачпропертиес](implementing-attachproperties.md)<br/>                          | Содержит описание и пример кода реализации функции [**аттачпропертиес**](attachproperties.md) , которая отделяет данные, распознаваемые синтаксическим анализатором, а затем прикрепляет описания свойств к каждому свойству протокола, существующему в распознанных данных.<br/> |
| <span id="Implementing_FormatProperties"></span><span id="implementing_formatproperties"></span><span id="IMPLEMENTING_FORMATPROPERTIES"></span>[Реализация Форматпропертиес](implementing-formatproperties.md)<br/>                          | Содержит описание и пример кода реализации функции [**форматпропертиес**](formatproperties.md) , которая форматирует данные, отображаемые в области сведений пользовательского интерфейса сетевой монитор.<br/>                                                                    |
| <span id="Implementing_Deregister"></span><span id="implementing_deregister"></span><span id="IMPLEMENTING_DEREGISTER"></span>[Реализация отмены регистрации](implementing-deregister.md)<br/>                                                        | Содержит описание и пример кода реализации функции [**дерегистрации**](deregister.md) , которая освобождает ресурсы, используемые для регистрации свойств протокола.<br/>                                                                                                     |



 

 

 




