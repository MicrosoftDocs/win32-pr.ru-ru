---
description: При задании уровня проверки подлинности для приложения определяется степень проверки подлинности, выполняемая при вызове клиентом приложения.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Установка уровня проверки подлинности для серверного приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701225"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a><span data-ttu-id="d505d-103">Установка уровня проверки подлинности для серверного приложения</span><span class="sxs-lookup"><span data-stu-id="d505d-103">Setting an Authentication Level for a Server Application</span></span>

<span data-ttu-id="d505d-104">При задании уровня проверки подлинности для приложения определяется степень проверки подлинности, выполняемая при вызове клиентом приложения.</span><span class="sxs-lookup"><span data-stu-id="d505d-104">When you set an authentication level for an application, you determine what degree of authentication is performed when clients call into the application.</span></span> <span data-ttu-id="d505d-105">Более высокие уровни проверки подлинности обеспечивают большую безопасность и целостность данных, хотя обычно с некоторыми снижениями производительности.</span><span class="sxs-lookup"><span data-stu-id="d505d-105">Higher authentication levels provide greater security and data integrity, although usually with some performance degradation.</span></span> <span data-ttu-id="d505d-106">Дополнительные сведения см. в разделе [Проверка подлинности клиента](client-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="d505d-106">For more information, see [Client Authentication](client-authentication.md).</span></span>

<span data-ttu-id="d505d-107">**Выбор уровня проверки подлинности для серверного приложения**</span><span class="sxs-lookup"><span data-stu-id="d505d-107">**To select an authentication level for a server application**</span></span>

1.  <span data-ttu-id="d505d-108">Щелкните правой кнопкой мыши приложение COM+, для которого задается проверка подлинности, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="d505d-108">Right-click the COM+ application for which you are setting authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="d505d-109">В диалоговом окне Свойства приложения перейдите на вкладку **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="d505d-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="d505d-110">В поле **уровень проверки подлинности для вызовов** выберите соответствующий уровень.</span><span class="sxs-lookup"><span data-stu-id="d505d-110">In the **Authentication level for calls** box, select the appropriate level.</span></span> <span data-ttu-id="d505d-111">Ниже приведены уровни, упорядоченные от минимального к более высокому уровню безопасности.</span><span class="sxs-lookup"><span data-stu-id="d505d-111">The levels are as follows, ordered from lowest to highest security:</span></span>

    -   <span data-ttu-id="d505d-112">**Нет**.</span><span class="sxs-lookup"><span data-stu-id="d505d-112">**None**.</span></span> <span data-ttu-id="d505d-113">Проверка подлинности не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d505d-113">No authentication occurs.</span></span>
    -   <span data-ttu-id="d505d-114">**Подключитесь**.</span><span class="sxs-lookup"><span data-stu-id="d505d-114">**Connect**.</span></span> <span data-ttu-id="d505d-115">Проверяет подлинность учетных данных только при установке соединения.</span><span class="sxs-lookup"><span data-stu-id="d505d-115">Authenticates credentials only when the connection is made.</span></span>
    -   <span data-ttu-id="d505d-116">**Вызов метода**.</span><span class="sxs-lookup"><span data-stu-id="d505d-116">**Call**.</span></span> <span data-ttu-id="d505d-117">Проверяет подлинность учетных данных в начале каждого вызова.</span><span class="sxs-lookup"><span data-stu-id="d505d-117">Authenticates credentials at the beginning of every call.</span></span>
    -   <span data-ttu-id="d505d-118">**Пакет**.</span><span class="sxs-lookup"><span data-stu-id="d505d-118">**Packet**.</span></span> <span data-ttu-id="d505d-119">Проверяет подлинность учетных данных и целостность полученных данных вызова.</span><span class="sxs-lookup"><span data-stu-id="d505d-119">Authenticates credentials and verifies that all call data is received.</span></span> <span data-ttu-id="d505d-120">Это значение по умолчанию для серверных приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="d505d-120">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="d505d-121">**Целостность пакетов**.</span><span class="sxs-lookup"><span data-stu-id="d505d-121">**Packet Integrity**.</span></span> <span data-ttu-id="d505d-122">Проверяет подлинность учетных данных и неизменность данных вызова при передаче.</span><span class="sxs-lookup"><span data-stu-id="d505d-122">Authenticates credentials and verifies that no call data has been modified in transit.</span></span>
    -   <span data-ttu-id="d505d-123">**Конфиденциальность пакетов**.</span><span class="sxs-lookup"><span data-stu-id="d505d-123">**Packet Privacy**.</span></span> <span data-ttu-id="d505d-124">Проверяет подлинность учетных данных и шифрует пакет, включая данные, а также удостоверение и подпись отправителя.</span><span class="sxs-lookup"><span data-stu-id="d505d-124">Authenticates credentials and encrypts the packet, including the data and the sender's identity and signature.</span></span>

4.  <span data-ttu-id="d505d-125">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d505d-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d505d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d505d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d505d-127">Включение проверки подлинности для библиотечного приложения</span><span class="sxs-lookup"><span data-stu-id="d505d-127">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



