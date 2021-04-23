---
description: Вопросы безопасности COM+ CRM
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Вопросы безопасности COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141223"
---
# <a name="com-crm-security-considerations"></a><span data-ttu-id="afe28-103">Вопросы безопасности COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="afe28-103">COM+ CRM Security Considerations</span></span>

<span data-ttu-id="afe28-104">Файл журнала CRM может содержать конфиденциальные сведения, которые должны быть защищены.</span><span class="sxs-lookup"><span data-stu-id="afe28-104">A CRM log file could contain sensitive information that must be secured.</span></span> <span data-ttu-id="afe28-105">По этой причине, если серверное приложение выполняется с любым удостоверением, Кроме интерактивного пользователя при первом создании файла журнала CRM, файл журнала CRM защищен только этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="afe28-105">For this reason, if the server application is running under any identity other than Interactive User when the CRM log file is first created, the CRM log file is security protected for that user only.</span></span> <span data-ttu-id="afe28-106">Эта функция доступна только в файловой системе NTFS.</span><span class="sxs-lookup"><span data-stu-id="afe28-106">This feature is available only on the NTFS file system.</span></span> <span data-ttu-id="afe28-107">Если впоследствии удостоверение серверного приложения изменилось, сведения о безопасности для файла журнала CRM не изменяются автоматически.</span><span class="sxs-lookup"><span data-stu-id="afe28-107">If the identity of the server application is subsequently changed, the security information for the CRM log file is not automatically changed.</span></span> <span data-ttu-id="afe28-108">Его можно изменить вручную с помощью существующих средств администрирования Windows.</span><span class="sxs-lookup"><span data-stu-id="afe28-108">It can be changed manually by using existing Windows administration tools.</span></span> <span data-ttu-id="afe28-109">В качестве альтернативы можно просто удалить файл журнала CRM, если он находится в чистом состоянии (что ожидается после управляемого завершения работы серверного приложения).</span><span class="sxs-lookup"><span data-stu-id="afe28-109">The alternative is simply to delete the CRM log file when it is in a clean state (which is expected after a controlled shutdown of the server application).</span></span>

<span data-ttu-id="afe28-110">При нормальной работе COM+ создает компонент CRM Compensator и вызывает интерфейс [**икрмкомпенсатор**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) .</span><span class="sxs-lookup"><span data-stu-id="afe28-110">In normal operation, COM+ creates the CRM compensator component and calls the [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) interface.</span></span> <span data-ttu-id="afe28-111">Однако пользователь, имеющий привилегии на создание компенсатора CRM, может вызвать интерфейс **икрмкомпенсатор** в недостаточное время, что может привести к проблемам безопасности системы.</span><span class="sxs-lookup"><span data-stu-id="afe28-111">However, a user having privileges to create the CRM Compensator can call the **ICrmCompensator** interface at inappropriate times, possibly causing system security problems.</span></span> <span data-ttu-id="afe28-112">Чтобы помочь защититься от этих проблем безопасности, системный администратор может использовать безопасность на основе ролей, чтобы ограничить компонент CRM Compensator только теми идентификаторами серверных приложений, в которых он работает.</span><span class="sxs-lookup"><span data-stu-id="afe28-112">To help protect against these security problems, the system administrator can use role-based security to restrict the CRM Compensator component to only those identities of the server applications in which it runs.</span></span> <span data-ttu-id="afe28-113">Если компонент выполняется в библиотечном приложении, он будет включать все удостоверения серверных приложений.</span><span class="sxs-lookup"><span data-stu-id="afe28-113">If the component is running in a library application, this would include all the identities of the server applications.</span></span>

> [!Note]  
> <span data-ttu-id="afe28-114">Начиная с Windows Server 2003, чтобы предотвратить активацию извне серверного приложения, можно обеспечить более безопасную систему, пометив компонент CRM Compensator как частный.</span><span class="sxs-lookup"><span data-stu-id="afe28-114">Starting with Windows Server 2003, to help prevent activation from outside the server application, it is possible to further ensure a more secure system by marking the CRM Compensator component as private.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="afe28-115">См. также</span><span class="sxs-lookup"><span data-stu-id="afe28-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afe28-116">Основные понятия о компенсации диспетчер ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="afe28-116">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



