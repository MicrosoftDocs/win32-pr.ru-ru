---
title: Необходимые условия для установки расширения схемы
description: Чтобы изменить схему, убедитесь в наличии следующих прав и осведомлены о следующих правах, которые должны иметь достаточные права для изменения схемы.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 275f468df54b9ced3dcca0648e4cc3602ab71422
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104336460"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a><span data-ttu-id="89fad-103">Необходимые условия для установки расширения схемы</span><span class="sxs-lookup"><span data-stu-id="89fad-103">Prerequisites for Installing a Schema Extension</span></span>

<span data-ttu-id="89fad-104">Чтобы изменить схему, убедитесь в наличии следующих прав и осведомлены о следующих возможностях.</span><span class="sxs-lookup"><span data-stu-id="89fad-104">To modify the schema, ensure you have the following rights and are aware of the following information:</span></span>

-   <span data-ttu-id="89fad-105">Необходимо иметь достаточные права для изменения схемы.</span><span class="sxs-lookup"><span data-stu-id="89fad-105">You must have sufficient rights to modify the schema.</span></span> <span data-ttu-id="89fad-106">Схема содержит все определения данных для служб домен Active Directory для всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="89fad-106">The schema contains all of the data definitions for Active Directory Domain Services for the entire enterprise.</span></span> <span data-ttu-id="89fad-107">Для обновления схемы пользователь должен быть членом группы Администраторы схемы или иметь права на обновление схемы.</span><span class="sxs-lookup"><span data-stu-id="89fad-107">To update the schema, a user must be a member of the Schema Administrators group, or have been delegated the rights to update the schema.</span></span>
-   <span data-ttu-id="89fad-108">Вносить изменения в схему можно только на хозяине схемы.</span><span class="sxs-lookup"><span data-stu-id="89fad-108">You can only make schema changes at the schema master.</span></span> <span data-ttu-id="89fad-109">Дополнительные сведения см. [в разделе Обнаружение хозяина схемы](detecting-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="89fad-109">For more information, see [Detecting the Schema Master](detecting-the-schema-master.md).</span></span>
-   <span data-ttu-id="89fad-110">Хозяин схемы должен быть доступен для записи; то есть блокировка безопасности в реестре должна быть удалена.</span><span class="sxs-lookup"><span data-stu-id="89fad-110">The schema master must be writable; that is, the safety interlock in the registry must be removed.</span></span> <span data-ttu-id="89fad-111">Дополнительные сведения см. в разделе [Включение изменений схемы в хозяине схемы](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="89fad-111">For more information, see [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
-   <span data-ttu-id="89fad-112">Дополнительные сведения о том, как проверить возможность изменения хозяина схемы и изменить его параметры, см. в разделе "XADM: не удается обновить схему на основе владельца схемы" статьи Справка и поддержка в базе знаний по адресу [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span><span class="sxs-lookup"><span data-stu-id="89fad-112">For more information about how to check whether the schema master can be modified, and how to change its settings, see "XADM: Unable to Update the Schema on the Schema Owner" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span></span>

 

 




