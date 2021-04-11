---
description: Для создания пакета исправлений рекомендуется использовать средство создания исправлений, например Msimsp.exe и Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272785"
---
# <a name="patchwizdll"></a>Patchwiz.dll

Для создания пакета исправлений рекомендуется использовать средство создания исправлений, например [Msimsp.exe](msimsp-exe.md) и Patchwiz.dll. Patchwiz.dll версии 4,0 совместима с пакетами и исправлениями, созданными в более ранних версиях Patchwiz.dll. Средство Patchwiz.dll доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).

В Patchwiz.dll версии 4,0 имеется одна новая функция [уикреатепатчпаккажеекс (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), которая расширяет функциональные возможности [уикреатепатчпаккаже (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md). Эти функции принимают файл свойств создания исправления (PCP-файл) и создают [пакет исправлений](patch-packages.md)установщика.

PCP-файл представляет собой двоичный файл базы данных с тем же форматом, что и база данных установщик Windows (MSI-файл), но с другой схемой базы данных. Поэтому PCP-файл можно создать с помощью тех же средств, которые используются для базы данных установщика.

Вы можете создать PCP-файл с помощью редактора таблиц, например [Orca.exe](orca-exe.md) , чтобы ввести данные в пустую базу данных PCP, которая поставляется с пакетом SDK для установщик Windows, Template. PCP. Дополнительные сведения см. [в разделе Пример исправления небольшого обновления](a-small-update-patching-example.md).

В каждом файле. PCP необходимы следующие таблицы базы данных:

-   [Таблица свойств (Patchwiz.dll)](properties-table-patchwiz-dll-.md)
-   [Таблица Имажефамилиес (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md)
-   [Таблица Упградедимажес (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md)
-   [Таблица Таржетимажес (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md)

Следующие таблицы базы данных являются необязательными:

-   [\_Таблица Оптионалдата упградедфилес (Patchwiz.dll)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [Таблица Фамилифилеранжес (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)
-   [\_Таблица Оптионалдата таржетфилес (Patchwiz.dll)](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [Таблица Екстерналфилес (Patchwiz.dll)](externalfiles-table-patchwiz-dll-.md)
-   [Таблица Упградедфилестоигноре (Patchwiz.dll)](upgradedfilestoignore-table-patchwiz-dll-.md)

В PCP-файлах, имеющих Минимумрекуиредмсиверсион, равный 300 в таблице [свойств](properties-table-patchwiz-dll-.md) , требуется следующая таблица.

-   [Таблица Патчметадата (Patchwiz.dll)](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> Таблица является необязательной, если Минимумрекуиредмсиверсион не равно 300.

 

Версия Patchwiz.dll, выпущенная с установщик Windows 3,0, может автоматически формировать сведения о последовательности исправлений и добавлять их в [таблицу мсипатчсекуенце](msipatchsequence-table.md) нового исправления. [Таблицу патчсекуенце](patchsequence-table--patchwiz-dll-.md) можно использовать для ручного добавления сведений о последовательности обновлений в таблицу мсипатчсекуенце. Дополнительные сведения см. в разделе [Создание сведений о последовательности исправления](generating-patch-sequence-information---patchwiz-dll-.md).

Начиная с версии Patchwiz.dll 2,0, можно увеличить скорость последующего создания исправления с помощью [кэширования сведений об исправлениях (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).

Использование общедоступных символов для целевой платформы и двоичных файлов образа обновления позволяет сократить размер двоичного исправления примерно на одну половину. Дополнительные сведения см. [в разделе Использование символов для сокращения размера двоичного исправления](using-symbols-to-reduce-binary-patch-size.md).

Можно указать, что определенные регионы целевого файла будут сохранены при установке исправлений, а сведения в этих регионах будут сохранены. Дополнительные сведения см. в разделе [исправление выбранных регионов файла](patching-selected-regions-of-a-file.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Выпущенные версии, средства и распространяемые пакеты](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



