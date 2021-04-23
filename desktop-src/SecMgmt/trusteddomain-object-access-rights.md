---
description: Содержит список и описание прав доступа объекта Трустеддомаин.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Права доступа к объекту Трустеддомаин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f79dc44b54ff907cbe3d1f700cc673f75a40d57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682574"
---
# <a name="trusteddomain-object-access-rights"></a><span data-ttu-id="d12b4-103">Права доступа к объекту Трустеддомаин</span><span class="sxs-lookup"><span data-stu-id="d12b4-103">TrustedDomain Object Access Rights</span></span>

<span data-ttu-id="d12b4-104">Тип объекта [**трустеддомаин**](trusteddomain-object.md) имеет следующие типы доступа:</span><span class="sxs-lookup"><span data-stu-id="d12b4-104">The [**TrustedDomain**](trusteddomain-object.md) object type has the following access types:</span></span>



| <span data-ttu-id="d12b4-105">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="d12b4-105">Access type</span></span>                  | <span data-ttu-id="d12b4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d12b4-106">Description</span></span>                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d12b4-107">\_ \_ доменное имя доверенного запроса \_</span><span class="sxs-lookup"><span data-stu-id="d12b4-107">TRUSTED\_QUERY\_DOMAIN\_NAME</span></span> | <span data-ttu-id="d12b4-108">Этот тип доступа необходим для запроса имени доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="d12b4-108">This access type is needed to query the name of the trusted domain.</span></span>              |
| <span data-ttu-id="d12b4-109">ДОВЕРЕНные \_ наборы \_ контроллеров</span><span class="sxs-lookup"><span data-stu-id="d12b4-109">TRUSTED\_SET\_CONTROLLERS</span></span>    | <span data-ttu-id="d12b4-110">Этот тип доступа необходим для задания списка контроллеров доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="d12b4-110">This access type is needed to set the list of controllers of the trusted domain.</span></span> |
| <span data-ttu-id="d12b4-111">POSIX TRUSTed \_ Query \_</span><span class="sxs-lookup"><span data-stu-id="d12b4-111">TRUSTED\_QUERY\_POSIX</span></span>        | <span data-ttu-id="d12b4-112">Этот тип доступа необходим для получения смещения идентификатора POSIX доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="d12b4-112">This access type is needed to retrieve the Posix ID offset of a trusted domain.</span></span>  |
| <span data-ttu-id="d12b4-113">ДОВЕРЕНный \_ набор \_ POSIX</span><span class="sxs-lookup"><span data-stu-id="d12b4-113">TRUSTED\_SET\_POSIX</span></span>          | <span data-ttu-id="d12b4-114">Этот тип доступа необходим для установки смещения идентификатора POSIX доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="d12b4-114">This access type is needed to set the Posix ID offset of a trusted domain.</span></span>       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="d12b4-115">Универсальные маски доступа</span><span class="sxs-lookup"><span data-stu-id="d12b4-115">Generic Access Masks</span></span>

<span data-ttu-id="d12b4-116">Этот тип объекта имеет следующие универсальные сопоставления доступа:</span><span class="sxs-lookup"><span data-stu-id="d12b4-116">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a><span data-ttu-id="d12b4-117">Стандартные типы доступа</span><span class="sxs-lookup"><span data-stu-id="d12b4-117">Standard Access Types</span></span>

<span data-ttu-id="d12b4-118">Этот объект не поддерживает (необязательно) СИНХРОНИЗАЦИю стандартного типа доступа.</span><span class="sxs-lookup"><span data-stu-id="d12b4-118">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="d12b4-119">Поддерживаются все необходимые типы доступа.</span><span class="sxs-lookup"><span data-stu-id="d12b4-119">All required access types are supported.</span></span> <span data-ttu-id="d12b4-120">Маска всех поддерживаемых типов доступа для этого типа объектов:</span><span class="sxs-lookup"><span data-stu-id="d12b4-120">The mask of all supported access types for this object type is:</span></span>

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



