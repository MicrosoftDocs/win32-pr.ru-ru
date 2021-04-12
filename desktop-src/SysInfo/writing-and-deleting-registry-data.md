---
description: Приложение может использовать функцию RegSetValueEx для связывания значения и его данных с ключом. Список типов значений, поддерживаемых RegSetValueEx, см. в разделе Типы значений реестра.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Запись и удаление данных реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345032"
---
# <a name="writing-and-deleting-registry-data"></a><span data-ttu-id="c6ba6-104">Запись и удаление данных реестра</span><span class="sxs-lookup"><span data-stu-id="c6ba6-104">Writing and Deleting Registry Data</span></span>

<span data-ttu-id="c6ba6-105">Приложение может использовать функцию [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) для связывания значения и его данных с ключом.</span><span class="sxs-lookup"><span data-stu-id="c6ba6-105">An application can use the [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) function to associate a value and its data with a key.</span></span> <span data-ttu-id="c6ba6-106">Список типов значений, поддерживаемых **RegSetValueEx**, см. в разделе [типы значений реестра](registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="c6ba6-106">For a list of the value types supported by **RegSetValueEx**, see [Registry Value Types](registry-value-types.md).</span></span>

<span data-ttu-id="c6ba6-107">Чтобы удалить значение из ключа, приложение может использовать функцию [**регделетевалуе**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) .</span><span class="sxs-lookup"><span data-stu-id="c6ba6-107">To delete a value from a key, an application can use the [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) function.</span></span> <span data-ttu-id="c6ba6-108">Чтобы удалить ключ, можно использовать функцию [**регделетекэй**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) .</span><span class="sxs-lookup"><span data-stu-id="c6ba6-108">To delete a key, it can use the [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) function.</span></span> <span data-ttu-id="c6ba6-109">Удаленный ключ не удаляется до тех пор, пока последний его маркер не будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="c6ba6-109">A deleted key is not removed until the last handle to it has been closed.</span></span> <span data-ttu-id="c6ba6-110">Подразделы и значения не могут быть созданы в удаленном ключе.</span><span class="sxs-lookup"><span data-stu-id="c6ba6-110">Subkeys and values cannot be created under a deleted key.</span></span>

<span data-ttu-id="c6ba6-111">Невозможно заблокировать раздел реестра во время операции записи для синхронизации доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="c6ba6-111">It is not possible to lock a registry key during a write operation to synchronize access to the data.</span></span> <span data-ttu-id="c6ba6-112">Тем не менее можно управлять доступом к разделу реестра с помощью атрибутов безопасности.</span><span class="sxs-lookup"><span data-stu-id="c6ba6-112">However, you can control access to a registry key using security attributes.</span></span> <span data-ttu-id="c6ba6-113">Дополнительные сведения см. в разделе [раздел реестра Security and Access Rights](registry-key-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="c6ba6-113">For more information, see [Registry Key Security and Access Rights](registry-key-security-and-access-rights.md).</span></span>

<span data-ttu-id="c6ba6-114">В одной транзакции может быть выполнено более одной операции с реестром.</span><span class="sxs-lookup"><span data-stu-id="c6ba6-114">More than one registry operation can be performed within a single transaction.</span></span> <span data-ttu-id="c6ba6-115">Чтобы связать раздел реестра с транзакцией, приложение может использовать функцию [**регкреатекэйтрансактед**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) или [**регопенкэйтрансактед**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="c6ba6-115">To associate a registry key with a transaction, an application can use the [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) or [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) function.</span></span> <span data-ttu-id="c6ba6-116">Дополнительные сведения о транзакциях см. в разделе [Диспетчер транзакций ядра](/windows/desktop/Ktm/kernel-transaction-manager-portal).</span><span class="sxs-lookup"><span data-stu-id="c6ba6-116">For more information about transactions, see [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).</span></span>

 

 
