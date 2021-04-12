---
description: Чтобы обеспечить безопасность установки программного обеспечения, придерживайтесь этих рекомендаций при создании установщик Windows настраиваемого действия.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Рекомендации по защите настраиваемых действий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265228"
---
# <a name="guidelines-for-securing-custom-actions"></a><span data-ttu-id="fbbeb-103">Рекомендации по защите настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="fbbeb-103">Guidelines for Securing Custom Actions</span></span>

<span data-ttu-id="fbbeb-104">Соблюдение следующих рекомендаций при создании установщик Windows пакета с настраиваемыми действиями помогает поддерживать безопасную среду во время установки:</span><span class="sxs-lookup"><span data-stu-id="fbbeb-104">Adherence to the following guidelines when authoring a Windows Installer package with custom actions helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="fbbeb-105">Защитите дополнительные файлы, записанные настраиваемым действием.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-105">Secure any additional files written by your custom action.</span></span>
-   <span data-ttu-id="fbbeb-106">Проверьте длину буфера и допустимость всех данных, считанных настраиваемым действием.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-106">Check buffer lengths and validity of all data read by your custom action.</span></span> <span data-ttu-id="fbbeb-107">Сюда входят свойства, которые могут предоставлять данные настраиваемому действию, в частности те, которые используют открытые свойства, предоставленные пользователем.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-107">This includes properties that may supply data to your custom action, particularly those that use public properties provided by a user.</span></span>
-   <span data-ttu-id="fbbeb-108">Не полагайтесь на внешние библиотеки DLL, которые не являются доверенными для системы на всех платформах, на которых должен выполняться установочный пакет.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-108">Do not rely on external DLLs that are not trusted by the system on all platforms on which your installation package is intended to run.</span></span>
-   <span data-ttu-id="fbbeb-109">Тщательно продумайте, следует ли использовать настраиваемые действия, использующие [*повышенные*](e-gly.md) привилегии или олицетворение.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-109">Carefully consider whether to use custom actions that use [*elevated*](e-gly.md) privileges or impersonation.</span></span> <span data-ttu-id="fbbeb-110">Пользовательские действия, такие как "открыть URL-адрес после установки", "" запустить программное обеспечение после завершения установки "или" запустить файл ReadMe после завершения установки ", обычно не требуют повышенных привилегий для работы.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-110">Custom actions such as “open a URL after installation is completed,” “launch the software after installation is complete,” or “launch ReadMe after installation is complete” would not usually require elevated privileges to function.</span></span> <span data-ttu-id="fbbeb-111">Если настраиваемое действие должно выполняться с *повышенными* привилегиями, убедитесь, что код настраиваемого действия предотвращает переполнение буфера и случайную загрузку ненадежного кода.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-111">If your custom action must run with *elevated* privileges, be sure that the custom action code guards against buffer overruns and inadvertent loading of unsafe code.</span></span> <span data-ttu-id="fbbeb-112">Обратите внимание, что на этапе выполнения установки установщик передает сведения процессу с *повышенными* привилегиями и запускает скрипт.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-112">Note that during the execution phase of the installation, the installer passes information to a process with *elevated* privileges and runs the script.</span></span> <span data-ttu-id="fbbeb-113">Любые настраиваемые действия, выполняемые на этапе выполнения, могут выполняться с *повышенными* привилегиями.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-113">Any custom actions that run during the execution phase may run with *elevated* privileges.</span></span>
-   <span data-ttu-id="fbbeb-114">Соберите все сведения, предоставленные пользователем во время выполнения последовательности пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-114">Gather all information provided by the user during the UI sequence.</span></span> <span data-ttu-id="fbbeb-115">Не запрашивать у пользователя какие-либо сведения, которые нельзя задать с помощью общедоступного свойства.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-115">Do not prompt the user for any information that can't be set using a public property.</span></span>
-   <span data-ttu-id="fbbeb-116">Если настраиваемое действие сценария развертывает свойства, примите меры предосторожности о том, что пользовательское действие защищено от возможности внедрения сценария.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-116">If your script custom action expands properties, take precautions that the custom action is secured against the possibility of script injection.</span></span> <span data-ttu-id="fbbeb-117">Сценарий может быть записан в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="fbbeb-117">Script may be logged in clear text.</span></span>

<span data-ttu-id="fbbeb-118">См. также [Безопасность настраиваемых действий](custom-action-security.md).</span><span class="sxs-lookup"><span data-stu-id="fbbeb-118">See also [Custom Action Security](custom-action-security.md).</span></span>

 

 



