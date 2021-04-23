---
title: Класс MDM_Policy_User_Result01_Desktop02
description: '\_Класс политики MDM \_ user \_ Result01 \_ Desktop02 представляет доступные политики профиля папки.'
ms.assetid: dab89ac4-b857-474e-8fe5-6822fe06ac91
keywords:
- Класс MDM_Policy_User_Result01_Desktop02
- MDM_Policy_User_Result01_Desktop02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Desktop02
- MDM_Policy_User_Result01_Desktop02.InstanceID
- MDM_Policy_User_Result01_Desktop02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da6504176140b9e775c7b7f83e0f9835ce25b42c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071668"
---
# <a name="mdm_policy_user_result01_desktop02-class"></a><span data-ttu-id="dd2b7-105">\_Класс политики MDM \_ user \_ Result01 \_ Desktop02</span><span class="sxs-lookup"><span data-stu-id="dd2b7-105">MDM\_Policy\_User\_Result01\_Desktop02 class</span></span>

<span data-ttu-id="dd2b7-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="dd2b7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dd2b7-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="dd2b7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dd2b7-108">\_Класс политики MDM \_ user \_ Result01 \_ Desktop02 представляет доступные политики профиля папки.</span><span class="sxs-lookup"><span data-stu-id="dd2b7-108">The MDM\_Policy\_User\_Result01\_Desktop02 class represents the available folder profile policies.</span></span>

<span data-ttu-id="dd2b7-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dd2b7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2b7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd2b7-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Desktop02
{
  string InstanceID;
  string ParentID;
  string PreventUserRedirectionOfProfileFolders;
};
```

## <a name="members"></a><span data-ttu-id="dd2b7-111">Члены</span><span class="sxs-lookup"><span data-stu-id="dd2b7-111">Members</span></span>

<span data-ttu-id="dd2b7-112">Класс **\_ \_ user \_ Result01 \_ Desktop02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dd2b7-112">The **MDM\_Policy\_User\_Result01\_Desktop02** class has these types of members:</span></span>

-   [<span data-ttu-id="dd2b7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd2b7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd2b7-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd2b7-114">Properties</span></span>

<span data-ttu-id="dd2b7-115">Класс **\_ \_ user \_ Result01 \_ Desktop02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="dd2b7-115">The **MDM\_Policy\_User\_Result01\_Desktop02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd2b7-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd2b7-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2b7-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd2b7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd2b7-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd2b7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd2b7-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd2b7-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd2b7-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dd2b7-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2b7-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd2b7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd2b7-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd2b7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd2b7-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd2b7-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd2b7-124">превентусерредиректионофпрофилефолдерс</span><span class="sxs-lookup"><span data-stu-id="dd2b7-124">PreventUserRedirectionOfProfileFolders</span></span>](/windows/client-management/mdm/policy-csp-desktop#desktop-preventuserredirectionofprofilefolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2b7-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd2b7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd2b7-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd2b7-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd2b7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="dd2b7-127">Requirements</span></span>



| <span data-ttu-id="dd2b7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="dd2b7-128">Requirement</span></span> | <span data-ttu-id="dd2b7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="dd2b7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2b7-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd2b7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2b7-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dd2b7-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd2b7-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd2b7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2b7-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd2b7-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dd2b7-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd2b7-134">Namespace</span></span><br/>                | <span data-ttu-id="dd2b7-135">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="dd2b7-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dd2b7-136">MOF</span><span class="sxs-lookup"><span data-stu-id="dd2b7-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd2b7-137"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd2b7-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd2b7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="dd2b7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd2b7-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd2b7-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

