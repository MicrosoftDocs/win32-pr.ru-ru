---
description: Для пользователей по всему миру текстовые входные данные являются частью современных вычислительных систем, ведения блогов, комментирования, твитов, обмена мгновенными сообщениями и других типов текста. в Windows 8 проверка орфографии встроена в элементы управления для редактирования.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Об API проверки орфографии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e3c15594be003b67a6e0c9df62e234e8076cd4ea213bc08468f3bb72698f51f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754944"
---
# <a name="about-the-spell-checking-api"></a>Об API проверки орфографии

Для пользователей по всему миру текстовые входные данные являются частью современных вычислительных систем, ведения блогов, комментирования, твитов, обмена мгновенными сообщениями и других типов текста. в Windows 8 проверка орфографии встроена в элементы управления для редактирования.

Разработчики могут использовать API проверки орфографии в своих приложениях для использования доступных служб проверки орфографии. разработчики также могут создавать средства проверки орфографии, которые становятся поставщиками и интегрированы в Windowsную платформу проверки орфографии.

API проверки орфографии предназначен для использования профессиональными разработчиками C/C++ Windows COM-приложений. API проверки орфографии не поддерживается для служб Windows и ASP.NET.

## <a name="versioning"></a>Управление версиями

API проверки орфографии доступен, начиная с Windows 8 или Windows Server 2012. Будущие дополнения к API будут обрабатываться путем создания новых интерфейсов, которые можно определить с помощью [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на существующих.

## <a name="interfaces"></a>Интерфейсы

Все интерфейсы должны быть освобождены, если они больше не используются. Все возвращаемые (выходные параметры) **LPWSTR** строки (и элементы **лполестр** из [**иенумстринг**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) должны быть освобождены с помощью [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , если они больше не используются.

## <a name="error-handling"></a>Обработка ошибок

Ошибки возвращаются как **HRESULT** s. ИНТЕРФЕЙСЫ [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) и [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) не поддерживаются в этом API. Ошибки не являются особенно выполняемыми, за исключением неверных аргументов.

Коды стандартных ошибок RPC могут возвращаться любыми вызовами API, так как они находятся вне процедуры. Применяются стандартные времена ожидания RPC.

## <a name="security"></a>Безопасность

API проверки орфографии может загрузить внешний код (поставщики проверки орфографии). Он будет выполнять этот код вне процесса и в ограниченном контексте безопасности.

## <a name="dictionary-files"></a>Файлы словарей

Пользовательские словари для языка, содержащие содержимое для списков добавленных, исключаемых и автослов, находятся в папке% AppData% \\ \\ правописания Майкрософт \\ *<language tag>* . Имена файлов: Default. dic (добавлен), Default. исключенного (исключено) и Default. ACL (Автозамена). Файлы имеют формат открытого текста UTF-16 LE, который должен начинаться с соответствующей метки порядка байтов (BOM). Каждая строка содержит слово (в списках добавленных и исключенных слов) или пару автозамены с словами, разделенными вертикальной чертой (" \| ") (в списке автозамены). Другие файлы. dic,. исключенного и. ACL, находящиеся в каталоге, будут обнаружены службой проверки орфографии и добавлены в списки пользовательских слов. Эти файлы считаются доступны только для чтения и не изменяются с помощью API проверки орфографии.

## <a name="installing-a-spell-checking-provider"></a>Установка поставщика проверки орфографии

При установке поставщика проверки орфографии все файлы, которые он использует, должны размещаться в расположении, допускающем доступ на чтение из идентификатора SID ([идентификатора безопасности](../secauthz/security-identifiers.md)) "все пакеты приложений". Установка этой папки в папке "Program Files" работает правильно. Кроме того, поставщик должен задать некоторые ключи в реестре, чтобы он отображался в API проверки орфографии. В \_ \_ \_ \_ зависимости от того, должен ли он быть установлен только для текущего пользователя или для всех пользователей, он может находиться в кусте hKey «текущий пользователь куст» или на локальном компьютере hKey.


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



[Образец поставщика проверки орфографии](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) содержит пример регистрации, необходимый для установки поставщика.

Если вы создаете новые параметры проверки орфографии для поставщика проверки орфографии, см. инструкции по именованию в разделе [**иоптиондескриптион:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по API проверки орфографии](spell-checker-api-reference.md)
</dt> <dt>

[Пример проверки орфографии клиента](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[Пример поставщика проверки орфографии](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[**Иоптиондескриптион:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[**иенумстринг**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> </dl>

 

 
