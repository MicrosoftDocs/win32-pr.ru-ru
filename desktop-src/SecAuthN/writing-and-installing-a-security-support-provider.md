---
description: Конструкция SSPI позволяет записывать и добавлять дополнительные SSP в систему.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Написание и установка поставщика поддержки безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663567"
---
# <a name="writing-and-installing-a-security-support-provider"></a><span data-ttu-id="e0f11-103">Написание и установка поставщика поддержки безопасности</span><span class="sxs-lookup"><span data-stu-id="e0f11-103">Writing and Installing a Security Support Provider</span></span>

<span data-ttu-id="e0f11-104">Конструкция SSPI позволяет записывать и добавлять дополнительные SSP в систему.</span><span class="sxs-lookup"><span data-stu-id="e0f11-104">The design of SSPI enables additional SSPs to be written and added to the system.</span></span> <span data-ttu-id="e0f11-105">[*Поставщик общих служб*](../secgloss/s-gly.md) , относящийся к модели безопасности, можно разработать с относительной простотой или отличной сложностью в зависимости от уровня интеграции с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="e0f11-105">An [*SSP*](../secgloss/s-gly.md) specific to a security model can be developed with relative ease or great complexity, depending on the level of integration with the operating system.</span></span> <span data-ttu-id="e0f11-106">Клиентский поставщик общих служб, который разрешает подключения к новому типу сервера, может быть разработан очень быстро, в то время как полный поставщик общих служб, предоставляющий локальное олицетворение, потребует больших усилий.</span><span class="sxs-lookup"><span data-stu-id="e0f11-106">A client SSP that allows connections to a new type of server could be developed very quickly, whereas a full SSP that provides local impersonation would require more effort.</span></span>

<span data-ttu-id="e0f11-107">SSP устанавливаются путем обновления значения **reg \_ SZ** в реестре, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e0f11-107">SSPs are installed by updating a **REG\_SZ** value in the registry, located as follows:</span></span>

<span data-ttu-id="e0f11-108">**HKey \_ Локальный \_ компьютер** \\ **система** \\ **CurrentControlSet** \\ **элемент управления** \\ **секуритипровидерс**  =  *Provider1.dll, Provider2.dll,*...    </span><span class="sxs-lookup"><span data-stu-id="e0f11-108">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **SecurityProviders** = *Provider1.dll, Provider2.dll,*…</span></span><dl> <dt>

            Data type
</dt> <dd>            <span data-ttu-id="e0f11-109">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="e0f11-109">REG\_SZ</span></span></dd> </dl>

<span data-ttu-id="e0f11-110">Одна библиотека DLL может содержать несколько SSP.</span><span class="sxs-lookup"><span data-stu-id="e0f11-110">A single DLL can contain multiple SSPs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0f11-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e0f11-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0f11-112">Ограничения, касающихся регистрации и установки пакета безопасности</span><span class="sxs-lookup"><span data-stu-id="e0f11-112">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
