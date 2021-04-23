---
title: Имсрдпклиентсекуредсеттингс Аудиоредиректионмоде, свойство
description: Задает параметры перенаправления звука, указывающие, следует ли перенаправлять звуки или воспроизводить звуки на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Аудиоредиректионмоде
- Службы удаленных рабочих столов свойства Аудиоредиректионмоде, интерфейс Имсрдпклиентсекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс, свойство Аудиоредиректионмоде
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535570"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a><span data-ttu-id="47ff6-106">Свойство Имсрдпклиентсекуредсеттингс:: Аудиоредиректионмоде</span><span class="sxs-lookup"><span data-stu-id="47ff6-106">IMsRdpClientSecuredSettings::AudioRedirectionMode property</span></span>

<span data-ttu-id="47ff6-107">Задает параметры перенаправления звука, указывающие, следует ли перенаправлять звуки или воспроизводить звуки на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="47ff6-107">Specifies the audio redirection settings, which specify whether to redirect sounds or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="47ff6-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="47ff6-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47ff6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47ff6-109">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="47ff6-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="47ff6-110">Property value</span></span>

<span data-ttu-id="47ff6-111">Новые параметры.</span><span class="sxs-lookup"><span data-stu-id="47ff6-111">The new settings.</span></span> <span data-ttu-id="47ff6-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="47ff6-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="47ff6-113">0</span><span class="sxs-lookup"><span data-stu-id="47ff6-113">0</span></span>
</dt> <dd>

<span data-ttu-id="47ff6-114">Перенаправлять звуки на клиент.</span><span class="sxs-lookup"><span data-stu-id="47ff6-114">Redirect sounds to the client.</span></span> <span data-ttu-id="47ff6-115">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47ff6-115">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="47ff6-116">1</span><span class="sxs-lookup"><span data-stu-id="47ff6-116">1</span></span>
</dt> <dd>

<span data-ttu-id="47ff6-117">Воспроизводить звуки на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="47ff6-117">Play sounds at the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="47ff6-118">2</span><span class="sxs-lookup"><span data-stu-id="47ff6-118">2</span></span>
</dt> <dd>

<span data-ttu-id="47ff6-119">Отключить перенаправление звука; не воспроизводить звуки на сервере.</span><span class="sxs-lookup"><span data-stu-id="47ff6-119">Disable sound redirection; do not play sounds at the server.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="47ff6-120">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="47ff6-120">Error codes</span></span>

<span data-ttu-id="47ff6-121">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="47ff6-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="47ff6-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47ff6-122">Remarks</span></span>

<span data-ttu-id="47ff6-123">Эти свойства не могут быть заданы при соединении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="47ff6-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="47ff6-124">Дополнительные сведения см. в руководстве [по обеспечению безопасности клиента RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="47ff6-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="47ff6-125">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="47ff6-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47ff6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="47ff6-126">Requirements</span></span>



| <span data-ttu-id="47ff6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="47ff6-127">Requirement</span></span> | <span data-ttu-id="47ff6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="47ff6-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47ff6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47ff6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="47ff6-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47ff6-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="47ff6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47ff6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="47ff6-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47ff6-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="47ff6-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="47ff6-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="47ff6-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47ff6-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="47ff6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="47ff6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47ff6-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47ff6-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="47ff6-137">IID</span><span class="sxs-lookup"><span data-stu-id="47ff6-137">IID</span></span><br/>                      | <span data-ttu-id="47ff6-138">IID \_ имсрдпклиентсекуредсеттингс определен как 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="47ff6-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47ff6-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47ff6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47ff6-140">**имсрдпклиентсекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="47ff6-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





