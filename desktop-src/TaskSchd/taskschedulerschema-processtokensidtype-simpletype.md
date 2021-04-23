---
title: Простой тип Процесстокенсидтипе
description: Определяет возможные значения для элемента Процесстокенсидтипе (ПринЦипалтипе).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- планировщик задач простого типа Процесстокенсидтипе
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415229"
---
# <a name="processtokensidtype-simple-type"></a><span data-ttu-id="a5050-104">Простой тип Процесстокенсидтипе</span><span class="sxs-lookup"><span data-stu-id="a5050-104">processTokenSidType Simple Type</span></span>

<span data-ttu-id="a5050-105">Определяет возможные значения для элемента [**процесстокенсидтипе (принЦипалтипе)**](taskschedulerschema-processtokensidtype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a5050-105">Defines the possible values for the [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="a5050-106">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="a5050-106">Enumeration values</span></span>

<span data-ttu-id="a5050-107">Простой тип **процесстокенсидтипе** определяет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="a5050-107">The **processTokenSidType** simple type defines the following values.</span></span>



| <span data-ttu-id="a5050-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a5050-108">Value</span></span>        | <span data-ttu-id="a5050-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a5050-109">Description</span></span>                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5050-110">Нет</span><span class="sxs-lookup"><span data-stu-id="a5050-110">None</span></span>         | <span data-ttu-id="a5050-111">Задачи выполняются в процессе, который не содержит идентификатор безопасности токена процесса (изменения в списке групп токенов процессов не вносятся).</span><span class="sxs-lookup"><span data-stu-id="a5050-111">Tasks are run in a process that does not contain a process token SID (no changes will be made to the process token groups list).</span></span><br/> |
| <span data-ttu-id="a5050-112">С неограниченным доступом</span><span class="sxs-lookup"><span data-stu-id="a5050-112">Unrestricted</span></span> | <span data-ttu-id="a5050-113">Идентификатор безопасности задачи будет производным от полного пути задачи и будет добавлен в список групп токенов процесса.</span><span class="sxs-lookup"><span data-stu-id="a5050-113">A task SID will be derived from the full task path and will be added to the process token groups list.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="a5050-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a5050-114">Requirements</span></span>



| <span data-ttu-id="a5050-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a5050-115">Requirement</span></span> | <span data-ttu-id="a5050-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a5050-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a5050-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5050-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a5050-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a5050-118">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a5050-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5050-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a5050-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5050-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





