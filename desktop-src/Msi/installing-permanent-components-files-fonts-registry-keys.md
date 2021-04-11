---
description: Чтобы установить файл, шрифт или раздел реестра, чтобы он не был удален при удалении продукта, необходимо сделать все компоненты, содержащие файл, шрифт или раздел реестра, постоянными.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Установка постоянных компонентов, файлов, шрифтов, разделов реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081582"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a><span data-ttu-id="25005-103">Установка постоянных компонентов, файлов, шрифтов, разделов реестра</span><span class="sxs-lookup"><span data-stu-id="25005-103">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>

<span data-ttu-id="25005-104">Чтобы установить файл, шрифт или раздел реестра, чтобы он не был удален при удалении продукта, необходимо сделать все компоненты, содержащие файл, шрифт или раздел реестра, постоянными.</span><span class="sxs-lookup"><span data-stu-id="25005-104">To install a file, font, or registry key so that it is not removed when the product is uninstalled, the entire component containing the file, font, or registry key must be made permanent.</span></span> <span data-ttu-id="25005-105">Чтобы сделать компонент постоянным, установите **мсидбкомпонентаттрибутесперманент** в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="25005-105">To make a component permanent, set **msidbComponentAttributesPermanent** in the Attributes column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="25005-106">Обратите внимание, что установщик удаляет раздел реестра после удаления последнего значения или подраздела раздела.</span><span class="sxs-lookup"><span data-stu-id="25005-106">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="25005-107">Чтобы предотвратить удаление пустого раздела реестра при удалении, напишите фиктивное значение под ключом, который необходимо сохранить, и введите + в столбце имя [таблицы реестра](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="25005-107">To prevent an empty registry key from being removed on uninstall, write a dummy value under the key you need keep, and enter + in the Name column of the [Registry table](registry-table.md).</span></span>

 

 



