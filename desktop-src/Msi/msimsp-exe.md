---
description: Рекомендуемым методом для создания пакета исправлений является использование средств создания исправлений, таких как Msimsp.exe и Patchwiz.dll. средство Msimsp.exe доступно только в компонентах Windows SDK для разработчиков установщик Windows.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa82f2fbefc9046877f4f98cf4a3c126d94e6542b60076f0491bd0f311ee00a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627801"
---
# <a name="msimspexe"></a>Msimsp.exe

Рекомендуемым методом для создания пакета исправлений является использование средств создания исправлений, таких как Msimsp.exe и [Patchwiz.dll](patchwiz-dll.md). средство Msimsp.exe доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).

Msimsp.exe — это исполняемый файл, который вызывает [Patchwiz.dll](patchwiz-dll.md). Средство можно использовать для создания пакета исправлений путем передачи пути в файл свойств создания исправления (файл. PCP) и путь к создаваемому пакету исправлений. Мсимсп. ex можно также использовать для создания файла журнала и указания временной папки, в которой сохраняются преобразования, ящики и файлы, используемые для создания пакета исправлений.

Синтаксис командной строки для Msimsp.exe:

**Msimsp.exe-s** *\[ путь \] к файлу. PCP* **-p** *\[ путь к файлу \] MSP* **{Options}**

В параметрах командной строки не учитывается регистр, а вместо тире можно использовать разделители косой черты. Если параметры не указаны, Msimsp.exe отображает текущие значения свойств сводных данных.

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ путь к файлу \] . PCP_
</dt> <dd>

Это обязательный параметр, за которым должен следовать путь к файлу свойств создания исправления (расширение PCP). Дополнительные сведения см. в разделе [PatchWiz.dll](patchwiz-dll.md).

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_путь к MSP-файлу_
</dt> <dd>

Это обязательный параметр, а затем путь к создаваемому пакету исправлений (расширение MSP).

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_путь к временной папке_
</dt> <dd>

Необязательный элемент. , За которым следует путь к временной папке. Расположение по умолчанию:% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

Необязательный элемент. Сбой, если временная папка уже существует.

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_путь к файлу журнала_
</dt> <dd>

Необязательный элемент. , За которым следует путь к файлу журнала, описывающий процесс создания исправления и ошибки. Дополнительные сведения см. в разделе [возвращаемые значения для уикреатепатчпаккаже](return-values-for-uicreatepatchpackage.md).

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-LP**_путь к файлу журнала с данными о производительности_
</dt> <dd>

Необязательный элемент. , За которым следует путь к файлу журнала, описывающий процесс создания исправления и ошибки. Этот параметр записывает данные о производительности в файл журнала. Для этого параметра требуется версия 4,0 Patchwiz.dll.

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Необязательный элемент. Отображает диалоговое окно при успешном завершении создания исправления.

</dd> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Отображает справку по командной строке.

</dd> </dl>

> [!Note]
> Msimsp.exe может завершиться ошибкой при вызове Makecab.exe, если в столбце file [таблицы File](file-table.md) пакета установки различаются только регистр. Windows Установщик чувствителен к регистру и разрешает пакет установки, например в таблице ниже, только если comp1 и Comp2 установлены в разные каталоги. Однако в этом сценарии нельзя использовать Msimsp.exe или [Patchwiz.dll](patchwiz-dll.md) для создания исправления пакета, так как Msimsp.exe и Patchwiz.dll вызывают Makecab.exe, который не учитывает регистр.
> 
> Избегайте создания пакета установки, такого как Следующая частичная [таблица файлов](file-table.md).
> 
> | File       | Компонент\_ | FileName   |
> |------------|-------------|------------|
> | readMe.txt | Comp1       | readMe.txt |
> | ReadMe.txt | Comp2       | readMe.txt |


## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание пакета исправлений](creating-a-patch-package.md)
</dt> <dt>

[Пример небольшого обновления исправлений](a-small-update-patching-example.md)
</dt> <dt>

[Windows Средства разработки установщика](windows-installer-development-tools.md)
</dt> <dt>

[Выпущенные версии, средства и распространяемые пакеты](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



