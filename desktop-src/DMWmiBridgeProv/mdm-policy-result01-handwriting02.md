---
title: Класс MDM_Policy_Result01_Handwriting02
description: '\_Класс политики MDM \_ Result01 \_ Handwriting02 представляет режим по умолчанию для панели рукописного ввода.'
ms.assetid: b21d0208-210d-476f-9269-f8d8a3307f17
keywords:
- Класс MDM_Policy_Result01_Handwriting02
- MDM_Policy_Result01_Handwriting02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Handwriting02
- MDM_Policy_Result01_Handwriting02.InstanceID
- MDM_Policy_Result01_Handwriting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636dcfbb0d3bceaf60697d2aaa6e7f158a052bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136126"
---
# <a name="mdm_policy_result01_handwriting02-class"></a><span data-ttu-id="c7607-105">\_Класс политики MDM \_ Result01 \_ Handwriting02</span><span class="sxs-lookup"><span data-stu-id="c7607-105">MDM\_Policy\_Result01\_Handwriting02 class</span></span>

<span data-ttu-id="c7607-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c7607-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c7607-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c7607-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c7607-108">\_Класс политики MDM \_ Result01 \_ Handwriting02 представляет режим по умолчанию для панели рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c7607-108">The MDM\_Policy\_Result01\_Handwriting02 class represents the default mode for the handwriting panel.</span></span>

<span data-ttu-id="c7607-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c7607-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7607-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7607-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Handwriting02
{
  string InstanceID;
  string ParentID;
  sint32 PanelDefaultModeDocked;
};
```

## <a name="members"></a><span data-ttu-id="c7607-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c7607-111">Members</span></span>

<span data-ttu-id="c7607-112">Класс **\_ политики MDM \_ Result01 \_ Handwriting02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c7607-112">The **MDM\_Policy\_Result01\_Handwriting02** class has these types of members:</span></span>

-   [<span data-ttu-id="c7607-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c7607-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7607-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c7607-114">Properties</span></span>

<span data-ttu-id="c7607-115">Класс **\_ политики MDM \_ Result01 \_ Handwriting02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c7607-115">The **MDM\_Policy\_Result01\_Handwriting02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7607-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c7607-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7607-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c7607-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7607-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7607-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7607-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c7607-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c7607-120">панелдефаултмодедоккед</span><span class="sxs-lookup"><span data-stu-id="c7607-120">PanelDefaultModeDocked</span></span>](/windows/client-management/mdm/policy-csp-handwriting#handwriting-paneldefaultmodedocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7607-121">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c7607-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7607-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c7607-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c7607-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c7607-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7607-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c7607-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7607-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7607-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7607-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c7607-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7607-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c7607-127">Requirements</span></span>



| <span data-ttu-id="c7607-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c7607-128">Requirement</span></span> | <span data-ttu-id="c7607-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c7607-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7607-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7607-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c7607-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c7607-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7607-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7607-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c7607-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c7607-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c7607-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c7607-134">Namespace</span></span><br/>                | <span data-ttu-id="c7607-135">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="c7607-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c7607-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c7607-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7607-137"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7607-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7607-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c7607-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7607-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7607-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

