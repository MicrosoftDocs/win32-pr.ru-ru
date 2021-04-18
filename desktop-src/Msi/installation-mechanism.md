---
description: 'Успешный процесс установки состоит из двух этапов: приобретения и выполнения. Если установка завершилась неудачно, может произойти этап отката.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Механизм установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650620"
---
# <a name="installation-mechanism"></a><span data-ttu-id="ed483-104">Механизм установки</span><span class="sxs-lookup"><span data-stu-id="ed483-104">Installation Mechanism</span></span>

<span data-ttu-id="ed483-105">Успешный процесс установки состоит из двух этапов: приобретения и выполнения.</span><span class="sxs-lookup"><span data-stu-id="ed483-105">There are two phases to a successful installation process: acquisition and execution.</span></span> <span data-ttu-id="ed483-106">Если установка завершилась неудачно, может произойти этап отката.</span><span class="sxs-lookup"><span data-stu-id="ed483-106">If the installation is unsuccessful, a rollback phase may occur.</span></span>

## <a name="acquisition"></a><span data-ttu-id="ed483-107">Получение</span><span class="sxs-lookup"><span data-stu-id="ed483-107">Acquisition</span></span>

<span data-ttu-id="ed483-108">В начале фазы приобретения приложение или пользователь предписывает установщику установить компонент или приложение.</span><span class="sxs-lookup"><span data-stu-id="ed483-108">At the beginning of the acquisition phase, an application or a user instructs the installer to install a feature or an application.</span></span> <span data-ttu-id="ed483-109">Затем установщик проходит через действия, указанные в таблицах последовательности базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="ed483-109">The installer then progresses through the actions specified in the sequence tables of the installation database.</span></span> <span data-ttu-id="ed483-110">Эти действия запрашивают базу данных установки и создают скрипт, который предоставляет пошаговую процедуру для выполнения установки.</span><span class="sxs-lookup"><span data-stu-id="ed483-110">These actions query the installation database and generate a script that gives a step-by-step procedure for performing the installation.</span></span>

## <a name="execution"></a><span data-ttu-id="ed483-111">Выполнение</span><span class="sxs-lookup"><span data-stu-id="ed483-111">Execution</span></span>

<span data-ttu-id="ed483-112">На этапе выполнения установщик передает сведения процессу с повышенными привилегиями и запускает скрипт.</span><span class="sxs-lookup"><span data-stu-id="ed483-112">During the execution phase, the installer passes the information to a process with elevated privileges and runs the script.</span></span>

## <a name="rollback"></a><span data-ttu-id="ed483-113">Откат</span><span class="sxs-lookup"><span data-stu-id="ed483-113">Rollback</span></span>

<span data-ttu-id="ed483-114">Если установка завершается неудачно, установщик восстанавливает исходное состояние компьютера.</span><span class="sxs-lookup"><span data-stu-id="ed483-114">If an installation is unsuccessful, the installer restores the original state of the computer.</span></span> <span data-ttu-id="ed483-115">Когда установщик обрабатывает сценарий установки, он одновременно создает скрипт отката.</span><span class="sxs-lookup"><span data-stu-id="ed483-115">When the installer processes the installation script it simultaneously generates a rollback script.</span></span> <span data-ttu-id="ed483-116">Помимо скрипта отката, установщик сохраняет копию каждого файла, который он удаляет, во время установки.</span><span class="sxs-lookup"><span data-stu-id="ed483-116">In addition to the rollback script, the installer saves a copy of every file it deletes during the installation.</span></span> <span data-ttu-id="ed483-117">Эти файлы хранятся в скрытом системном каталоге.</span><span class="sxs-lookup"><span data-stu-id="ed483-117">These files are kept in a hidden, system directory.</span></span> <span data-ttu-id="ed483-118">После завершения установки сценарий отката и сохраненные файлы удаляются.</span><span class="sxs-lookup"><span data-stu-id="ed483-118">Once the installation is complete, the rollback script and the saved files are deleted.</span></span> <span data-ttu-id="ed483-119">Дополнительные сведения см. в разделе [ROLLBACK Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="ed483-119">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



