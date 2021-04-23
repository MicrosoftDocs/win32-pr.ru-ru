---
description: Список интерфейсов в API проверки подлинности.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Интерфейсы проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265023"
---
# <a name="authentication-interfaces"></a><span data-ttu-id="672f8-103">Интерфейсы проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="672f8-103">Authentication Interfaces</span></span>

<span data-ttu-id="672f8-104">Интерфейсы проверки подлинности делятся на категории по использованию следующим образом.</span><span class="sxs-lookup"><span data-stu-id="672f8-104">Authentication interfaces are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="672f8-105">Интерфейсы смарт-карт</span><span class="sxs-lookup"><span data-stu-id="672f8-105">Smart Card Interfaces</span></span>](#smart-card-interfaces)
-   [<span data-ttu-id="672f8-106">Интерфейсы совместного использования удостоверений</span><span class="sxs-lookup"><span data-stu-id="672f8-106">Identity Sharing Interfaces</span></span>](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a><span data-ttu-id="672f8-107">Интерфейсы смарт-карт</span><span class="sxs-lookup"><span data-stu-id="672f8-107">Smart Card Interfaces</span></span>

<span data-ttu-id="672f8-108">Пакет SDK для смарт-карт предоставляет следующие COM-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="672f8-108">The Smart Card SDK provides the following COM interfaces.</span></span> <span data-ttu-id="672f8-109">Методы для определенного интерфейса перечислены в содержании и на странице справки для этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="672f8-109">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="672f8-110">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="672f8-110">Interface</span></span>                                    | <span data-ttu-id="672f8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="672f8-111">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="672f8-112">**ибитебуффер**</span><span class="sxs-lookup"><span data-stu-id="672f8-112">**IByteBuffer**</span></span>](ibytebuffer.md)           | <span data-ttu-id="672f8-113">Управляет объектом потока.</span><span class="sxs-lookup"><span data-stu-id="672f8-113">Manages a stream object.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="672f8-114">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="672f8-114">**ISCard**</span></span>](iscard.md)                     | <span data-ttu-id="672f8-115">Открывает подключение к [*смарт-карте*](/windows/desktop/SecGloss/s-gly)и управляет им.</span><span class="sxs-lookup"><span data-stu-id="672f8-115">Opens and manages a connection to a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span>                                                                    |
| [<span data-ttu-id="672f8-116">**искардаус**</span><span class="sxs-lookup"><span data-stu-id="672f8-116">**ISCardAuth**</span></span>](iscardauth.md)             | <span data-ttu-id="672f8-117">Проверяет подлинность приложения, смарт-карты или пользователя.</span><span class="sxs-lookup"><span data-stu-id="672f8-117">Authenticates an application, smart card, or user.</span></span>                                                                                                                                       |
| [<span data-ttu-id="672f8-118">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="672f8-118">**ISCardCmd**</span></span>](iscardcmd.md)               | <span data-ttu-id="672f8-119">Конструирует и управляет [*блоком данных протокола приложений*](/windows/desktop/SecGloss/a-gly) смарт-карт (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="672f8-119">Constructs and manages a smart card [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) (APDU).</span></span> |
| [<span data-ttu-id="672f8-120">**искарддатабасе**</span><span class="sxs-lookup"><span data-stu-id="672f8-120">**ISCardDatabase**</span></span>](iscarddatabase.md)     | <span data-ttu-id="672f8-121">Выполняет операции с базой данных [*диспетчера ресурсов*](/windows/desktop/SecGloss/r-gly) смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="672f8-121">Performs smart card [*resource manager*](/windows/desktop/SecGloss/r-gly) database operations.</span></span>                                              |
| [<span data-ttu-id="672f8-122">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="672f8-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md) | <span data-ttu-id="672f8-123">Выполняет общие файловые службы, такие как поиск, выбор, чтение, запись, создание и удаление файлов.</span><span class="sxs-lookup"><span data-stu-id="672f8-123">Performs common file services such as locating, selecting, reading, writing, creating, and deleting files.</span></span>                                                                               |
| [<span data-ttu-id="672f8-124">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="672f8-124">**ISCardISO7816**</span></span>](iscardiso7816.md)       | <span data-ttu-id="672f8-125">Конструирует команду КАТЕГОРИЯХ APDU.</span><span class="sxs-lookup"><span data-stu-id="672f8-125">Constructs an APDU command.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="672f8-126">**искардлокате**</span><span class="sxs-lookup"><span data-stu-id="672f8-126">**ISCardLocate**</span></span>](iscardlocate.md)         | <span data-ttu-id="672f8-127">Находит смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="672f8-127">Locates a smart card.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="672f8-128">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="672f8-128">**ISCardManage**</span></span>](iscardmanage.md)         | <span data-ttu-id="672f8-129">Управляет системой смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="672f8-129">Manages the smart card system.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="672f8-130">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="672f8-130">**ISCardTypeConv**</span></span>](iscardtypeconv.md)     | <span data-ttu-id="672f8-131">Предоставляет методы, используемые для поддержки других интерфейсов COM смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="672f8-131">Provides methods used to support other smart card COM interfaces.</span></span> <span data-ttu-id="672f8-132">Этот интерфейс предоставляется только для обратной совместимости и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="672f8-132">This interface is provided for backward compatibility only and should no longer be used.</span></span>                               |
| [<span data-ttu-id="672f8-133">**искардверифи**</span><span class="sxs-lookup"><span data-stu-id="672f8-133">**ISCardVerify**</span></span>](iscardverify.md)         | <span data-ttu-id="672f8-134">Проверяет или изменяет политику проверки владельца карты (ЧВ).</span><span class="sxs-lookup"><span data-stu-id="672f8-134">Verifies or changes card holder verification (CHV) policy.</span></span>                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a><span data-ttu-id="672f8-135">Интерфейсы совместного использования удостоверений</span><span class="sxs-lookup"><span data-stu-id="672f8-135">Identity Sharing Interfaces</span></span>

<span data-ttu-id="672f8-136">Пакет SDK для совместного использования удостоверений предоставляет следующие COM-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="672f8-136">The Identity Sharing SDK provides the following COM interfaces.</span></span> <span data-ttu-id="672f8-137">Методы для определенного интерфейса перечислены в содержании и на странице справки для этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="672f8-137">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="672f8-138">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="672f8-138">Interface</span></span>                                                          | <span data-ttu-id="672f8-139">Описание</span><span class="sxs-lookup"><span data-stu-id="672f8-139">Description</span></span>                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="672f8-140">**иассоЦиатедидентитипровидер**</span><span class="sxs-lookup"><span data-stu-id="672f8-140">**IAssociatedIdentityProvider**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | <span data-ttu-id="672f8-141">Позволяет поставщику удостоверений связывать удостоверения с локальными учетными записями пользователей.</span><span class="sxs-lookup"><span data-stu-id="672f8-141">Allows an identity provider to associate identities with local user accounts.</span></span>            |
| [<span data-ttu-id="672f8-142">**иидентитядвисе**</span><span class="sxs-lookup"><span data-stu-id="672f8-142">**IIdentityAdvise**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | <span data-ttu-id="672f8-143">Позволяет поставщику удостоверений уведомлять вызывающее приложение об обновлении удостоверения.</span><span class="sxs-lookup"><span data-stu-id="672f8-143">Allows an identity provider to notify a calling application when an identity is updated.</span></span> |
| [<span data-ttu-id="672f8-144">**иидентитипровидер**</span><span class="sxs-lookup"><span data-stu-id="672f8-144">**IIdentityProvider**</span></span>](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | <span data-ttu-id="672f8-145">Представляет поставщик удостоверений.</span><span class="sxs-lookup"><span data-stu-id="672f8-145">Represents an identity provider.</span></span>                                                         |
| [<span data-ttu-id="672f8-146">**иидентитисторе**</span><span class="sxs-lookup"><span data-stu-id="672f8-146">**IIdentityStore**</span></span>](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | <span data-ttu-id="672f8-147">Предоставляет методы для перечисления и управления удостоверениями и поставщиками удостоверений.</span><span class="sxs-lookup"><span data-stu-id="672f8-147">Provides methods to enumerate and manage identities and identity providers.</span></span>              |



 

 

 
