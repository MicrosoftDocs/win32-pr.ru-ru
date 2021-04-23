---
title: Рекомендации по проекту
description: Рекомендации по проекту
ms.assetid: aebe2886-0af0-443a-a5be-651f11936639
keywords:
- Пакет SDK для Windows Media Format, рекомендации по проекту
- Расширенный формат систем (ASF), рекомендации по проекту
- ASF (Расширенный системный формат), рекомендации по проекту
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1682e8008569c9b230b2c2f53f394326669d022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258969"
---
# <a name="project-considerations"></a><span data-ttu-id="39d76-106">Рекомендации по проекту</span><span class="sxs-lookup"><span data-stu-id="39d76-106">Project Considerations</span></span>

<span data-ttu-id="39d76-107">Необходимо убедиться, что конечный пользователь может правильно запускать приложения, созданные с помощью пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="39d76-107">You must ensure that the end user can properly run applications that you create with the Windows Media Format SDK.</span></span> <span data-ttu-id="39d76-108">В этом разделе описаны две вещи, которые необходимо учитывать при распространении приложений, расширений имен файлов и распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="39d76-108">This section describes two things you must consider when distributing applications, file name extensions and software redistribution.</span></span>

<span data-ttu-id="39d76-109">Необходимо использовать правильные расширения имен файлов для всех файлов, созданных в приложениях.</span><span class="sxs-lookup"><span data-stu-id="39d76-109">You must use the correct file name extensions for any files created with your applications.</span></span> <span data-ttu-id="39d76-110">Использование правильных расширений имен файлов упрощает распознавание файлов ASF и предотвращает путаницу при декодировании файлов.</span><span class="sxs-lookup"><span data-stu-id="39d76-110">Using proper file name extensions makes it easier for end users to recognize ASF files and prevents confusion when decoding files.</span></span>

<span data-ttu-id="39d76-111">Необходимо предоставить все распространяемые компоненты, необходимые для запуска приложений.</span><span class="sxs-lookup"><span data-stu-id="39d76-111">You must provide any redistributables that are required to run your applications.</span></span> <span data-ttu-id="39d76-112">Без правильных распространяемых пакетов пользователи не смогут использовать ваши приложения.</span><span class="sxs-lookup"><span data-stu-id="39d76-112">Without the correct redistributables, users will not be able to use your applications.</span></span>

<span data-ttu-id="39d76-113">В следующих разделах подробно описаны расширения имен файлов и повторное распространение программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="39d76-113">The following sections describe file name extensions and software redistribution in detail.</span></span>



| <span data-ttu-id="39d76-114">Section</span><span class="sxs-lookup"><span data-stu-id="39d76-114">Section</span></span>                                                                      | <span data-ttu-id="39d76-115">Описание</span><span class="sxs-lookup"><span data-stu-id="39d76-115">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39d76-116">Рекомендации по расширению имени файла</span><span class="sxs-lookup"><span data-stu-id="39d76-116">File Name Extension Guidelines</span></span>](file-name-extension-guidelines.md)         | <span data-ttu-id="39d76-117">Содержит сведения о расширениях имен файлов, которые следует использовать для файлов ASF, создаваемых программой.</span><span class="sxs-lookup"><span data-stu-id="39d76-117">Provides information about the file name extensions you should use for ASF files that your program creates.</span></span>     |
| [<span data-ttu-id="39d76-118">Повторное распространение программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="39d76-118">Software Redistribution</span></span>](software-redistribution.md)                       | <span data-ttu-id="39d76-119">Описание распространяемых компонентов пакета SDK для формата Windows Media и способов их включения в приложения.</span><span class="sxs-lookup"><span data-stu-id="39d76-119">Describes the redistributables for the Windows Media Format SDK and how to include them with your applications.</span></span> |
| [<span data-ttu-id="39d76-120">Регистрация зависимости приложения</span><span class="sxs-lookup"><span data-stu-id="39d76-120">Registering Application Dependency</span></span>](registering-application-dependency.md) | <span data-ttu-id="39d76-121">Описание процесса регистрации приложения в зависимости от среды выполнения пакета SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="39d76-121">Describes how to register your application as being dependent on the Windows Media Format SDK runtime.</span></span>          |



 

 

 




