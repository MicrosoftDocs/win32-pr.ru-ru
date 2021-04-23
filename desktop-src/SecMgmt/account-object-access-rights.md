---
description: Тип прав доступа к объекту учетной записи имеет следующие типы доступа.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Права доступа к объекту учетной записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546223"
---
# <a name="account-object-access-rights"></a><span data-ttu-id="3dced-103">Права доступа к объекту учетной записи</span><span class="sxs-lookup"><span data-stu-id="3dced-103">Account Object Access Rights</span></span>

<span data-ttu-id="3dced-104">Тип прав доступа к объекту учетной записи имеет следующие типы доступа.</span><span class="sxs-lookup"><span data-stu-id="3dced-104">The Account Object Access Rights type has the following access types.</span></span>



| <span data-ttu-id="3dced-105">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="3dced-105">Access type</span></span>                     | <span data-ttu-id="3dced-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3dced-106">Description</span></span>                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dced-107">представление УЧЕТной записи \_</span><span class="sxs-lookup"><span data-stu-id="3dced-107">ACCOUNT\_VIEW</span></span>                   | <span data-ttu-id="3dced-108">Этот тип доступа необходим для чтения сведений об учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3dced-108">This access type is required to read the account information.</span></span> <span data-ttu-id="3dced-109">К ним относятся [*привилегии*](/windows/desktop/SecGloss/p-gly) , назначенные учетной записи, назначенные квоты памяти, а также специальные предоставленные типы доступа.</span><span class="sxs-lookup"><span data-stu-id="3dced-109">This includes the [*privileges*](/windows/desktop/SecGloss/p-gly) assigned to the account, memory quotas assigned, and any special access types granted.</span></span> |
| <span data-ttu-id="3dced-110">\_права на изменение учетной записи \_</span><span class="sxs-lookup"><span data-stu-id="3dced-110">ACCOUNT\_ADJUST\_PRIVILEGES</span></span>     | <span data-ttu-id="3dced-111">Этот тип доступа необходим для назначения привилегий или удаления привилегий из учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3dced-111">This access type is required to assign privileges to or remove privileges from an account.</span></span>                                                                                                                                                            |
| <span data-ttu-id="3dced-112">\_Настройка \_ квот для УЧЕТной записи</span><span class="sxs-lookup"><span data-stu-id="3dced-112">ACCOUNT\_ADJUST\_QUOTAS</span></span>         | <span data-ttu-id="3dced-113">Этот тип доступа требуется для изменения системных квот, назначенных учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3dced-113">This access type is required to change the system quotas assigned to an account.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="3dced-114">УЧЕТная запись \_ Настройка \_ \_ доступа к системе</span><span class="sxs-lookup"><span data-stu-id="3dced-114">ACCOUNT\_ADJUST\_SYSTEM\_ACCESS</span></span> | <span data-ttu-id="3dced-115">Этот тип доступа необходим для обновления флагов доступа к системе для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3dced-115">This access type is required to update the system access flags for the account.</span></span>                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="3dced-116">Универсальные маски доступа</span><span class="sxs-lookup"><span data-stu-id="3dced-116">Generic Access Masks</span></span>

<span data-ttu-id="3dced-117">Объект [**Account**](account-object.md) публикует следующие сопоставления из универсальных типов доступа к конкретным типам доступа.</span><span class="sxs-lookup"><span data-stu-id="3dced-117">The [**Account**](account-object.md) object publishes the following mappings from generic access types to specific access types.</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="3dced-118">Стандартные типы доступа</span><span class="sxs-lookup"><span data-stu-id="3dced-118">Standard Access Types</span></span>

<span data-ttu-id="3dced-119">Этот объект не поддерживает (необязательно) СИНХРОНИЗАЦИю стандартного типа доступа.</span><span class="sxs-lookup"><span data-stu-id="3dced-119">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="3dced-120">Поддерживаются все необходимые типы доступа.</span><span class="sxs-lookup"><span data-stu-id="3dced-120">All required access types are supported.</span></span> <span data-ttu-id="3dced-121">Ниже приведена маска всех поддерживаемых типов доступа для этого типа объектов.</span><span class="sxs-lookup"><span data-stu-id="3dced-121">The mask of all supported access types for this object type is as follows.</span></span>

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
