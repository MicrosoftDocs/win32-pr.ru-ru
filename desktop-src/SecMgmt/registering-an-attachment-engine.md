---
description: Прежде чем подсистема настройки безопасности сможет вызвать обработчик вложений для обработки задач, зависящих от службы, необходимо установить подсистему вложений и зарегистрировать ее в подсистеме настройки безопасности.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Регистрация подсистемы вложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682583"
---
# <a name="registering-an-attachment-engine"></a><span data-ttu-id="bffa5-103">Регистрация подсистемы вложений</span><span class="sxs-lookup"><span data-stu-id="bffa5-103">Registering an Attachment Engine</span></span>

<span data-ttu-id="bffa5-104">Прежде чем подсистема настройки безопасности сможет вызвать обработчик вложений для обработки задач, зависящих от службы, необходимо установить подсистему вложений и зарегистрировать ее в подсистеме настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="bffa5-104">Before the Security Configuration Engine can call your attachment engine to process service-specific tasks, you must install your attachment engine and register it with the Security Configuration Engine.</span></span>

<span data-ttu-id="bffa5-105">**Установка и регистрация библиотеки DLL подсистемы вложений**</span><span class="sxs-lookup"><span data-stu-id="bffa5-105">**To install and register the attachment engine DLL**</span></span>

1.  <span data-ttu-id="bffa5-106">Скопируйте библиотеку DLL подсистемы вложений в каталог в системе.</span><span class="sxs-lookup"><span data-stu-id="bffa5-106">Copy the attachment engine DLL to a directory on the system.</span></span> <span data-ttu-id="bffa5-107">Предпочтительный каталог —% WINDIR% \\ secedit \\ .</span><span class="sxs-lookup"><span data-stu-id="bffa5-107">The preferred directory is %windir%\\secedit\\attachments.</span></span> <span data-ttu-id="bffa5-108">Если этот каталог не существует, его следует создать.</span><span class="sxs-lookup"><span data-stu-id="bffa5-108">If this directory does not exist, you should create it.</span></span>
2.  <span data-ttu-id="bffa5-109">Создайте раздел реестра в следующем узле.</span><span class="sxs-lookup"><span data-stu-id="bffa5-109">Create a registry key under the following node.</span></span> <span data-ttu-id="bffa5-110">*Имя службы* — это зарегистрированное имя для вложения. оно должно совпадать с именем службы, используемым в диспетчере управления службами, модулем, который управляет остановкой и запуском служб.</span><span class="sxs-lookup"><span data-stu-id="bffa5-110">The *service name* is the registered name for the attachment, and must be the same service name used in the Service Control Manager, a module which manages the stopping and starting of services.</span></span> <span data-ttu-id="bffa5-111">Имя также должно быть уникальным, поэтому оно не конфликтует с именами других вложений.</span><span class="sxs-lookup"><span data-stu-id="bffa5-111">The name must also be unique so it does not conflict with the names of other attachments.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  <span data-ttu-id="bffa5-112">Создайте следующее строковое значение в новом разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="bffa5-112">Create the following string value in the new registry key.</span></span> <span data-ttu-id="bffa5-113">*путь к подсистеме вложений* — это полный путь к модулю подсистемы вложений.</span><span class="sxs-lookup"><span data-stu-id="bffa5-113">*attachment engine path* is the full path to the attachment engine module.</span></span><dl> <dd><span data-ttu-id="bffa5-114">**Сервицеаттачментпас**  =  *путь к подсистеме вложений*</span><span class="sxs-lookup"><span data-stu-id="bffa5-114">**ServiceAttachmentPath** = *attachment engine path*</span></span><dl> <dt>

<span data-ttu-id="bffa5-115">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bffa5-115">Data type</span></span>
</dt> <dd><span data-ttu-id="bffa5-116">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bffa5-116">REG_SZ</span></span></dd> </dl> </dd> </dl>

 

 



