---
title: Имсрдпклиентсекуредсеттингс Кэйбоардхукмоде, свойство
description: Задает параметры перенаправления клавиатуры, определяющие способ и время применения сочетания клавиш Windows (например, ALT + TAB).
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Кэйбоардхукмоде
- Службы удаленных рабочих столов свойства Кэйбоардхукмоде, интерфейс Имсрдпклиентсекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс, свойство Кэйбоардхукмоде
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 948069b689d8799a98805148017a204b719d7645
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415169"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a><span data-ttu-id="84748-106">Свойство Имсрдпклиентсекуредсеттингс:: Кэйбоардхукмоде</span><span class="sxs-lookup"><span data-stu-id="84748-106">IMsRdpClientSecuredSettings::KeyboardHookMode property</span></span>

<span data-ttu-id="84748-107">Задает параметры перенаправления клавиатуры, определяющие способ и время применения сочетания клавиш Windows (например, ALT + TAB).</span><span class="sxs-lookup"><span data-stu-id="84748-107">Specifies the keyboard redirection settings, which specify how and when to apply Windows keyboard shortcut (for example, ALT+TAB).</span></span>

<span data-ttu-id="84748-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="84748-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="84748-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84748-109">Syntax</span></span>


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a><span data-ttu-id="84748-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="84748-110">Property value</span></span>

<span data-ttu-id="84748-111">Новые параметры.</span><span class="sxs-lookup"><span data-stu-id="84748-111">The new settings.</span></span> <span data-ttu-id="84748-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="84748-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="84748-113">0</span><span class="sxs-lookup"><span data-stu-id="84748-113">0</span></span>
</dt> <dd>

<span data-ttu-id="84748-114">Применение сочетаний клавиш только локально на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="84748-114">Apply key combinations only locally at the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="84748-115">1</span><span class="sxs-lookup"><span data-stu-id="84748-115">1</span></span>
</dt> <dd>

<span data-ttu-id="84748-116">Применение сочетаний клавиш на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="84748-116">Apply key combinations at the remote server.</span></span>

</dd> <dt>

<span data-ttu-id="84748-117">2</span><span class="sxs-lookup"><span data-stu-id="84748-117">2</span></span>
</dt> <dd>

<span data-ttu-id="84748-118">Сочетания клавиш применяются к удаленному серверу только в том случае, если клиент работает в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="84748-118">Apply key combinations to the remote server only when the client is running in full-screen mode.</span></span> <span data-ttu-id="84748-119">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84748-119">This is the default value.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="84748-120">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="84748-120">Error codes</span></span>

<span data-ttu-id="84748-121">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="84748-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="84748-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84748-122">Remarks</span></span>

<span data-ttu-id="84748-123">Эти свойства не могут быть заданы при соединении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="84748-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="84748-124">Дополнительные сведения см. в руководстве [по обеспечению безопасности клиента RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="84748-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="84748-125">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="84748-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84748-126">Требования</span><span class="sxs-lookup"><span data-stu-id="84748-126">Requirements</span></span>



| <span data-ttu-id="84748-127">Требование</span><span class="sxs-lookup"><span data-stu-id="84748-127">Requirement</span></span> | <span data-ttu-id="84748-128">Значение</span><span class="sxs-lookup"><span data-stu-id="84748-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84748-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84748-129">Minimum supported client</span></span><br/> | <span data-ttu-id="84748-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84748-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="84748-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84748-131">Minimum supported server</span></span><br/> | <span data-ttu-id="84748-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84748-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="84748-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="84748-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="84748-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84748-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="84748-135">DLL</span><span class="sxs-lookup"><span data-stu-id="84748-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84748-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84748-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="84748-137">IID</span><span class="sxs-lookup"><span data-stu-id="84748-137">IID</span></span><br/>                      | <span data-ttu-id="84748-138">IID \_ имсрдпклиентсекуредсеттингс определен как 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="84748-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84748-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84748-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84748-140">**имсрдпклиентсекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="84748-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





