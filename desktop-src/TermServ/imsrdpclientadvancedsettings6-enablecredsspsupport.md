---
title: IMsRdpClientAdvancedSettings6 Енаблекредсспсуппорт, свойство
description: Указывает, включен ли поставщик службы безопасности учетных данных (CredSSP) для этого подключения.
ms.assetid: 3BC8A265-7AEA-4C9C-9730-7710E1A3159D
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Енаблекредсспсуппорт
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.put_EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73ad2b024cd0f8bbcafd6ba05be093c5953d54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534142"
---
# <a name="imsrdpclientadvancedsettings6enablecredsspsupport-property"></a><span data-ttu-id="55506-110">Свойство IMsRdpClientAdvancedSettings6:: Енаблекредсспсуппорт</span><span class="sxs-lookup"><span data-stu-id="55506-110">IMsRdpClientAdvancedSettings6::EnableCredSspSupport property</span></span>

<span data-ttu-id="55506-111">Указывает, включен ли поставщик службы безопасности учетных данных (CredSSP) для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="55506-111">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="55506-112">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="55506-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="55506-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55506-113">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="55506-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="55506-114">Property value</span></span>

<span data-ttu-id="55506-115">Указывает, включен ли CredSSP для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="55506-115">Specifies whether CredSSP is enabled for this connection.</span></span> <span data-ttu-id="55506-116">Установите значение **\_ true** , чтобы включить CredSSP или **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="55506-116">Set to **VARIANT\_TRUE** to enable CredSSP or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="55506-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55506-117">Remarks</span></span>

<span data-ttu-id="55506-118">Это свойство поддерживается только клиентами подключение к удаленному рабочему столу 6,1 и 7,0.</span><span class="sxs-lookup"><span data-stu-id="55506-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="55506-119">Требования</span><span class="sxs-lookup"><span data-stu-id="55506-119">Requirements</span></span>



| <span data-ttu-id="55506-120">Требование</span><span class="sxs-lookup"><span data-stu-id="55506-120">Requirement</span></span> | <span data-ttu-id="55506-121">Значение</span><span class="sxs-lookup"><span data-stu-id="55506-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55506-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55506-122">Minimum supported client</span></span><br/> | <span data-ttu-id="55506-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55506-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="55506-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55506-124">Minimum supported server</span></span><br/> | <span data-ttu-id="55506-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55506-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="55506-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="55506-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="55506-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55506-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="55506-128">DLL</span><span class="sxs-lookup"><span data-stu-id="55506-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55506-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55506-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="55506-130">IID</span><span class="sxs-lookup"><span data-stu-id="55506-130">IID</span></span><br/>                      | <span data-ttu-id="55506-131">IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="55506-131">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55506-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55506-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55506-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="55506-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="55506-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="55506-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="55506-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="55506-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





