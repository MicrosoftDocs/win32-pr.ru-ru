---
title: Имстсксекуредсеттингс WorkDir, свойство
description: Указывает рабочий каталог запускаемой программы.
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства WorkDir
- Службы удаленных рабочих столов свойства WorkDir, интерфейс Имстсксекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имстсксекуредсеттингс, свойство WorkDir
- Службы удаленных рабочих столов свойства WorkDir, интерфейс Имсрдпклиентсекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс, свойство WorkDir
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0a80b35ba682012150b4277d800bc4a3582e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672881"
---
# <a name="imstscsecuredsettingsworkdir-property"></a><span data-ttu-id="5cf7d-108">Свойство Имстсксекуредсеттингс:: WorkDir</span><span class="sxs-lookup"><span data-stu-id="5cf7d-108">IMsTscSecuredSettings::WorkDir property</span></span>

<span data-ttu-id="5cf7d-109">Указывает рабочий каталог запускаемой программы.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-109">Specifies the working directory of the start program.</span></span>

<span data-ttu-id="5cf7d-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf7d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cf7d-111">Syntax</span></span>


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a><span data-ttu-id="5cf7d-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5cf7d-112">Property value</span></span>

<span data-ttu-id="5cf7d-113">Новый рабочий каталог.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-113">The new working directory.</span></span> <span data-ttu-id="5cf7d-114">Максимальная длина этой строки равна максимальному **\_ пути**-1 символам.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5cf7d-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5cf7d-115">Error codes</span></span>

<span data-ttu-id="5cf7d-116">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="5cf7d-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cf7d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5cf7d-117">Remarks</span></span>

<span data-ttu-id="5cf7d-118">Дополнительные сведения см. в руководстве [по обеспечению безопасности клиента RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf7d-118">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="5cf7d-119">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5cf7d-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf7d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5cf7d-120">Requirements</span></span>



| <span data-ttu-id="5cf7d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5cf7d-121">Requirement</span></span> | <span data-ttu-id="5cf7d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5cf7d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf7d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5cf7d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5cf7d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5cf7d-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5cf7d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5cf7d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5cf7d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cf7d-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5cf7d-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5cf7d-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="5cf7d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cf7d-128"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="5cf7d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5cf7d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cf7d-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cf7d-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="5cf7d-131">IID</span><span class="sxs-lookup"><span data-stu-id="5cf7d-131">IID</span></span><br/>                      | <span data-ttu-id="5cf7d-132">IID \_ имстсксекуредсеттингс определен как c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="5cf7d-132">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cf7d-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cf7d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf7d-134">**имсрдпклиентсекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="5cf7d-134">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5cf7d-135">**имстсксекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="5cf7d-135">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





