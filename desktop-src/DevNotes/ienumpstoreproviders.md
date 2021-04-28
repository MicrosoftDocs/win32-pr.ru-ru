---
description: Интерфейс Иенумпсторепровидерс — предоставляет стандартные методы перечисления COM для интерфейса Ипсторе.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Интерфейс Иенумпсторепровидерс (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089352"
---
# <a name="ienumpstoreproviders-interface"></a><span data-ttu-id="9db73-103">Интерфейс Иенумпсторепровидерс</span><span class="sxs-lookup"><span data-stu-id="9db73-103">IEnumPStoreProviders interface</span></span>

<span data-ttu-id="9db73-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9db73-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="9db73-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="9db73-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="9db73-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="9db73-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="9db73-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="9db73-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="9db73-108">Предоставляет стандартные методы перечисления COM для интерфейса [**ипсторе**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="9db73-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="9db73-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="9db73-109">Members</span></span>

<span data-ttu-id="9db73-110">Интерфейс **иенумпсторепровидерс** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9db73-110">The **IEnumPStoreProviders** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9db73-111">**Иенумпсторепровидерс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9db73-111">**IEnumPStoreProviders** also has these types of members:</span></span>

-   [<span data-ttu-id="9db73-112">Методы</span><span class="sxs-lookup"><span data-stu-id="9db73-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9db73-113">Методы</span><span class="sxs-lookup"><span data-stu-id="9db73-113">Methods</span></span>

<span data-ttu-id="9db73-114">Интерфейс **иенумпсторепровидерс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9db73-114">The **IEnumPStoreProviders** interface has these methods.</span></span>



| <span data-ttu-id="9db73-115">Метод</span><span class="sxs-lookup"><span data-stu-id="9db73-115">Method</span></span>                                      | <span data-ttu-id="9db73-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9db73-116">Description</span></span>                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9db73-117">**Clone (Клонировать)**</span><span class="sxs-lookup"><span data-stu-id="9db73-117">**Clone**</span></span>](ienumpstoreproviders-clone.md) | <span data-ttu-id="9db73-118">Создает другой перечислитель с тем же состоянием перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="9db73-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="9db73-119">**Далее**</span><span class="sxs-lookup"><span data-stu-id="9db73-119">**Next**</span></span>](ienumpstoreproviders-next.md)   | <span data-ttu-id="9db73-120">Возвращает следующий указанный поставщик в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="9db73-120">Gets the next specified provider in the enumeration sequence.</span></span><br/>                           |
| [<span data-ttu-id="9db73-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="9db73-121">**Reset**</span></span>](ienumpstoreproviders-reset.md) | <span data-ttu-id="9db73-122">Выполняет сброс до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="9db73-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="9db73-123">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="9db73-123">**Skip**</span></span>](ienumpstoreproviders-skip.md)   | <span data-ttu-id="9db73-124">Пропускает указанный поставщик в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="9db73-124">Skips the specified provider in the enumeration sequence.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="9db73-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9db73-125">Requirements</span></span>



| <span data-ttu-id="9db73-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9db73-126">Requirement</span></span> | <span data-ttu-id="9db73-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9db73-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9db73-128">Header</span><span class="sxs-lookup"><span data-stu-id="9db73-128">Header</span></span><br/> | <dl> <span data-ttu-id="9db73-129"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="9db73-129"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="9db73-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9db73-130">DLL</span></span><br/>    | <dl> <span data-ttu-id="9db73-131"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db73-131"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
