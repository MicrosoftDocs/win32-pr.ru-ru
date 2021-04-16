---
title: Класс MDM_Policy_Config01_Messaging02
description: '\_Класс политики MDM \_ Config01 \_ Messaging02 обеспечивает резервное копирование и восстановление текстовых сообщений, а также обмен сообщениями по всему миру. Эта политика позволяет Организации отключить эти функции, чтобы избежать хранения данных на серверах, не входящих в их управление.'
ms.assetid: 179ece8a-d3f4-449c-8392-ca8a35e44a31
keywords:
- Класс MDM_Policy_Config01_Messaging02
- MDM_Policy_Config01_Messaging02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Messaging02
- MDM_Policy_Config01_Messaging02.InstanceID
- MDM_Policy_Config01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137d9c36a822cd93d6cfd0c7cd83197204fb8f97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534121"
---
# <a name="mdm_policy_config01_messaging02-class"></a><span data-ttu-id="443da-106">\_Класс политики MDM \_ Config01 \_ Messaging02</span><span class="sxs-lookup"><span data-stu-id="443da-106">MDM\_Policy\_Config01\_Messaging02 class</span></span>

<span data-ttu-id="443da-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="443da-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="443da-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="443da-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="443da-109">\_Класс политики MDM \_ Config01 \_ Messaging02 обеспечивает резервное копирование и восстановление текстовых сообщений, а также обмен сообщениями по всему миру.</span><span class="sxs-lookup"><span data-stu-id="443da-109">The MDM\_Policy\_Config01\_Messaging02 class enables text message back up and restore and Messaging Everywhere.</span></span> <span data-ttu-id="443da-110">Эта политика позволяет Организации отключить эти функции, чтобы избежать хранения данных на серверах, не входящих в их управление.</span><span class="sxs-lookup"><span data-stu-id="443da-110">This policy allows an organization to disable these features to avoid information being stored on servers outside of their control.</span></span>

<span data-ttu-id="443da-111">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="443da-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="443da-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="443da-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a><span data-ttu-id="443da-113">Члены</span><span class="sxs-lookup"><span data-stu-id="443da-113">Members</span></span>

<span data-ttu-id="443da-114">Класс **\_ политики MDM \_ Config01 \_ Messaging02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="443da-114">The **MDM\_Policy\_Config01\_Messaging02** class has these types of members:</span></span>

-   [<span data-ttu-id="443da-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="443da-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="443da-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="443da-116">Properties</span></span>

<span data-ttu-id="443da-117">Класс **\_ политики MDM \_ Config01 \_ Messaging02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="443da-117">The **MDM\_Policy\_Config01\_Messaging02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="443da-118">алловмессажесинк</span><span class="sxs-lookup"><span data-stu-id="443da-118">AllowMessageSync</span></span>](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="443da-119">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="443da-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="443da-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="443da-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="443da-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="443da-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="443da-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="443da-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="443da-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="443da-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="443da-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="443da-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="443da-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="443da-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="443da-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="443da-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="443da-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="443da-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="443da-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="443da-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="443da-129">Требования</span><span class="sxs-lookup"><span data-stu-id="443da-129">Requirements</span></span>



| <span data-ttu-id="443da-130">Требование</span><span class="sxs-lookup"><span data-stu-id="443da-130">Requirement</span></span> | <span data-ttu-id="443da-131">Значение</span><span class="sxs-lookup"><span data-stu-id="443da-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="443da-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="443da-132">Minimum supported client</span></span><br/> | <span data-ttu-id="443da-133">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="443da-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="443da-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="443da-134">Minimum supported server</span></span><br/> | <span data-ttu-id="443da-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="443da-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="443da-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="443da-136">Namespace</span></span><br/>                | <span data-ttu-id="443da-137">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="443da-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="443da-138">MOF</span><span class="sxs-lookup"><span data-stu-id="443da-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="443da-139"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="443da-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="443da-140">DLL</span><span class="sxs-lookup"><span data-stu-id="443da-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="443da-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="443da-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

