---
description: Метод Connect объекта MERGE можно использовать для подключения модуля к дополнительному компоненту, который был объединен с базой данных или который будет объединен в базу данных. Функция должна существовать до вызова этого метода.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Подключение модуля слияния к нескольким функциям
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911663"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a><span data-ttu-id="d4c59-104">Подключение модуля слияния к нескольким функциям</span><span class="sxs-lookup"><span data-stu-id="d4c59-104">Connecting a Merge Module to Multiple Features</span></span>

<span data-ttu-id="d4c59-105">Метод [**Connect**](merge-connect.md) [объекта Merge](merge-object.md) можно использовать для подключения модуля к дополнительному компоненту, который был объединен с базой данных или который будет объединен в базу данных.</span><span class="sxs-lookup"><span data-stu-id="d4c59-105">The [**Connect**](merge-connect.md) method of the [Merge Object](merge-object.md) can be used to connect a module to an additional feature that has been merged into the database or that will be merged into the database.</span></span> <span data-ttu-id="d4c59-106">Функция должна существовать до вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="d4c59-106">The feature must exist before calling this method.</span></span>

<span data-ttu-id="d4c59-107">Модуль слияния никогда не должен доставлять компонент, содержащий системные файлы, основному компоненту приложения, так как это может привести к тому, что установщик будет проверять и восстанавливать приложение каждый раз при использовании системного файла.</span><span class="sxs-lookup"><span data-stu-id="d4c59-107">A merge module should never deliver a component containing system files to the main feature of an application, because this may cause the Installer to validate and repair the application each time the system file is used.</span></span> <span data-ttu-id="d4c59-108">Должен быть создан MSI-файл, предназначенный для приема компонентов из модуля слияния, чтобы все компоненты, содержащие системные файлы, принадлежали только к компонентам, которые отделены от основной функции приложения.</span><span class="sxs-lookup"><span data-stu-id="d4c59-108">A .msi file that is intended to accept components from a merge module should be authored so that any components that contain system files only belong to features that are separate from the main feature of the application.</span></span>

<span data-ttu-id="d4c59-109">Если пакет использует модуль слияния, содержащий системные файлы, связывающие все компоненты из модуля слияния с основным компонентом приложения, попытка использовать системный файл может вызвать запуск установщика для попыток восстановления основной функции приложения.</span><span class="sxs-lookup"><span data-stu-id="d4c59-109">If your package uses a merge module containing system files that link all the components from the merge module to the main feature of the application, an attempt to use the system file may trigger the Installer to try and repair the main feature of the application.</span></span> <span data-ttu-id="d4c59-110">Если невозможно восстановить основную функцию, может произойти сбой установки.</span><span class="sxs-lookup"><span data-stu-id="d4c59-110">If the main feature cannot be repaired, the installation may fail.</span></span>

 

 



