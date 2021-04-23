---
title: Класс MDM_Policy_User_Result01_CredentialsUI02
description: '\_ \_ \_ Класс User RESULT01 CredentialsUI02 политики MDM \_ представляет доступные политики учетных данных.'
ms.assetid: e1df7798-676a-4846-89e5-2c05d0259086
keywords:
- Класс MDM_Policy_User_Result01_CredentialsUI02
- MDM_Policy_User_Result01_CredentialsUI02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_CredentialsUI02
- MDM_Policy_User_Result01_CredentialsUI02.InstanceID
- MDM_Policy_User_Result01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7659990ee980872059bd26b0a8b553202e6cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071669"
---
# <a name="mdm_policy_user_result01_credentialsui02-class"></a><span data-ttu-id="3f93b-105">\_Класс политики MDM \_ user \_ Result01 \_ CredentialsUI02</span><span class="sxs-lookup"><span data-stu-id="3f93b-105">MDM\_Policy\_User\_Result01\_CredentialsUI02 class</span></span>

<span data-ttu-id="3f93b-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="3f93b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3f93b-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="3f93b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3f93b-108">\_ \_ \_ Класс User RESULT01 CredentialsUI02 политики MDM \_ представляет доступные политики учетных данных.</span><span class="sxs-lookup"><span data-stu-id="3f93b-108">The MDM\_Policy\_User\_Result01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="3f93b-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3f93b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f93b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f93b-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
};
```

## <a name="members"></a><span data-ttu-id="3f93b-111">Члены</span><span class="sxs-lookup"><span data-stu-id="3f93b-111">Members</span></span>

<span data-ttu-id="3f93b-112">Класс **\_ \_ user \_ Result01 \_ CredentialsUI02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3f93b-112">The **MDM\_Policy\_User\_Result01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="3f93b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3f93b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f93b-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3f93b-114">Properties</span></span>

<span data-ttu-id="3f93b-115">Класс **\_ \_ user \_ Result01 \_ CredentialsUI02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="3f93b-115">The **MDM\_Policy\_User\_Result01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3f93b-116">дисаблепассвордревеал</span><span class="sxs-lookup"><span data-stu-id="3f93b-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f93b-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f93b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f93b-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3f93b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3f93b-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3f93b-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f93b-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f93b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f93b-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f93b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f93b-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3f93b-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3f93b-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3f93b-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f93b-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f93b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f93b-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f93b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f93b-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3f93b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f93b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="3f93b-127">Requirements</span></span>



| <span data-ttu-id="3f93b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="3f93b-128">Requirement</span></span> | <span data-ttu-id="3f93b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="3f93b-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f93b-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f93b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3f93b-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3f93b-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f93b-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f93b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3f93b-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3f93b-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3f93b-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3f93b-134">Namespace</span></span><br/>                | <span data-ttu-id="3f93b-135">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="3f93b-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3f93b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3f93b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f93b-137"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f93b-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f93b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3f93b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f93b-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f93b-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

