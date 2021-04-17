---
title: Перечисление WMDM_FIND_SCOPE
description: '\_ \_ Тип перечисления вмдм Find SCOPE определяет область объекта хранилища.'
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- WMDM_FIND_SCOPE перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694603"
---
# <a name="wmdm_find_scope-enumeration"></a><span data-ttu-id="9b95a-104">\_Перечисление вмдм поиска \_ области</span><span class="sxs-lookup"><span data-stu-id="9b95a-104">WMDM\_FIND\_SCOPE enumeration</span></span>

<span data-ttu-id="9b95a-105">Тип перечисления **вмдм \_ Find \_ Scope** определяет область объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="9b95a-105">The **WMDM\_FIND\_SCOPE** enumeration type defines the scope of the storage object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b95a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b95a-106">Syntax</span></span>


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a><span data-ttu-id="9b95a-107">Константы</span><span class="sxs-lookup"><span data-stu-id="9b95a-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9b95a-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**ВМДМ \_ найти \_ область \_ Global**</span><span class="sxs-lookup"><span data-stu-id="9b95a-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM\_FIND\_SCOPE\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="9b95a-109">Поиск совпадающего объекта в любом месте на устройстве.</span><span class="sxs-lookup"><span data-stu-id="9b95a-109">Looking for the matching object anywhere on the device.</span></span>

</dd> <dt>

<span data-ttu-id="9b95a-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**\_ \_ \_ непосредственные \_ дочерние элементы вмдм поиска области**</span><span class="sxs-lookup"><span data-stu-id="9b95a-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM\_FIND\_SCOPE\_IMMEDIATE\_CHILDREN**</span></span>
</dt> <dd>

<span data-ttu-id="9b95a-111">Поиск соответствующего объекта в этом хранилище и его дочерних элементах.</span><span class="sxs-lookup"><span data-stu-id="9b95a-111">Looking for the matching object within this storage and its children.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b95a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="9b95a-112">Requirements</span></span>



| <span data-ttu-id="9b95a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="9b95a-113">Requirement</span></span> | <span data-ttu-id="9b95a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9b95a-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9b95a-115">Header</span><span class="sxs-lookup"><span data-stu-id="9b95a-115">Header</span></span><br/> | <dl> <span data-ttu-id="9b95a-116"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9b95a-116"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b95a-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b95a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b95a-118">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="9b95a-118">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





