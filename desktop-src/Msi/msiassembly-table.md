---
description: В таблице Мсиассембли указаны параметры установщик Windows для сборок платформы Microsoft .NET и сборок Win32. Дополнительные сведения см. в разделе Установка сборок в глобальный кэш сборок и установка сборок Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Таблица Мсиассембли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999595"
---
# <a name="msiassembly-table"></a>Таблица Мсиассембли

В таблице Мсиассембли указаны параметры установщик Windows для сборок платформы Microsoft .NET и сборок Win32. Дополнительные сведения см. [в разделе Установка сборок в глобальный кэш сборок](installation-of-assemblies-to-the-global-assembly-cache.md) и [Установка сборок Win32](installation-of-win32-assemblies.md).

В Windows XP установщик Windows может устанавливать сборки Win32 как [Параллельные сборки](side-by-side-assemblies.md). Дополнительные сведения см. в разделе [параллельная сборка API](../sbscs/side-by-side-assembly-api.md).

**Windows 2000:** Эта функция не поддерживается.

Таблица Мсиассембли содержит следующие столбцы.



| Столбец            | Type                         | Ключ | Допускает значения NULL |
|-------------------|------------------------------|-----|----------|
| Компонент\_       | [Идентификатор](identifier.md) | Да   | Нет        |
| Функция\_         | [Идентификатор](identifier.md) | Нет   | Нет        |
| \_Манифест файла    | [Идентификатор](identifier.md) | Нет   | Да        |
| \_Приложение файла | [Идентификатор](identifier.md) | Нет   | Да        |
| Атрибуты        | [Integer](integer.md)       | Нет   | Да        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Ключ в [таблице Component](component-table.md) , указывающий компонент установщик Windows, который содержит эту сборку.

Значение в этом поле не должно быть равно null. Поле ключевого пути компонента в [таблице Component](component-table.md) не должно иметь значение null.

Для сборок Win32 ключевой путь к компоненту не может быть файлом манифеста, указанным в файле \_ manifest. Манифест может быть ключевой страницей для платформа .NET Framework или сборки политики.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_
</dt> <dd>

Ключ в [таблицу функций](feature-table.md).

Если сборка должна быть установлена при установке компонента, установщик Windows устанавливает компонент, указанный в этом поле.

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>\_Манифест файла
</dt> <dd>

Внешний ключ в [таблице File](file-table.md) , указывающий файл, содержащий манифест сборки платформа .NET Framework или сборки Win32.

Для сборки Win32 не указывайте этот файл в качестве файла пути к ключу компонента в поле ключевой путь [таблицы Component](component-table.md).

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>\_Приложение файла
</dt> <dd>

Чтобы установить сборку в частном расположении, введите в этом поле файл пути к ключу для компонента сборки.

Это значение, которое отображается в поле ключевого пути [таблицы Component](component-table.md). Установщик может установить сборку в структуру каталогов компонента, указанного в [таблице Directory](directory-table.md). Если сборка должна быть установлена в глобальный кэш сборок, это поле должно иметь значение null.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибута
</dt> <dd>

Введите значение 1 (одно) для сборки Win32. Введите значение 0 (ноль) для платформа .NET Framework сборки.

Если столбец Attributes имеет значение NULL, установщик рассматривает сборку как сборку платформа .NET Framework.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если в таблице Мсиассембли есть хотя бы одна запись, [Таблица инсталлексекутесекуенце](installexecutesequence-table.md) должна содержать [действие Мсипублишассемблиес](msipublishassemblies-action.md)и [мсиунпублишассемблиес действие](msiunpublishassemblies-action.md).

Поскольку откат сборок после их фиксации невозможен, установщик Windows использует двухэтапный процесс установки. Интерфейсы для сборок создаются во время операций установки, создаваемых [действием мсипублишассемблиес](msipublishassemblies-action.md).

Сборки не фиксируются до успешного выполнения [действия функции InstallFinalize](installfinalize-action.md). Это означает, что при создании настраиваемого действия или ресурса, основанного на сборке, она должна быть упорядочена после [действия функции InstallFinalize](installfinalize-action.md). Например, если необходимо запустить службу, которая зависит от сборки в глобальном кэше сборок (GAC), необходимо запланировать запуск этой службы после выполнения [действия функции InstallFinalize](installfinalize-action.md). Это означает, что нельзя использовать [таблицу ServiceControl](servicecontrol-table.md) для запуска службы, вместо этого необходимо использовать настраиваемое действие, виртуализированное после функции InstallFinalize.

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 
