---
title: Имстсксекуредсеттингс Стартпрограм, свойство
description: Указывает программу, запускаемую на удаленном сервере при подключении.
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Стартпрограм
- Службы удаленных рабочих столов свойства Стартпрограм, интерфейс Имстсксекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имстсксекуредсеттингс, свойство Стартпрограм
- Службы удаленных рабочих столов свойства Стартпрограм, интерфейс Имсрдпклиентсекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс, свойство Стартпрограм
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682116"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a><span data-ttu-id="d1c8a-108">Свойство Имстсксекуредсеттингс:: Стартпрограм</span><span class="sxs-lookup"><span data-stu-id="d1c8a-108">IMsTscSecuredSettings::StartProgram property</span></span>

<span data-ttu-id="d1c8a-109">Указывает программу, запускаемую на удаленном сервере при подключении.</span><span class="sxs-lookup"><span data-stu-id="d1c8a-109">Specifies the program to be started on the remote server upon connection.</span></span>

<span data-ttu-id="d1c8a-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d1c8a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c8a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1c8a-111">Syntax</span></span>


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a><span data-ttu-id="d1c8a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d1c8a-112">Property value</span></span>

<span data-ttu-id="d1c8a-113">Имя новой программы запуска.</span><span class="sxs-lookup"><span data-stu-id="d1c8a-113">The name of the new start program.</span></span> <span data-ttu-id="d1c8a-114">Максимальная длина этой строки равна максимальному **\_ пути**-1 символам.</span><span class="sxs-lookup"><span data-stu-id="d1c8a-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d1c8a-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d1c8a-115">Error codes</span></span>

<span data-ttu-id="d1c8a-116">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="d1c8a-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1c8a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1c8a-117">Remarks</span></span>

<span data-ttu-id="d1c8a-118">Если значение этого свойства не задано, будет запущена команда оболочки пользователя сеанса.</span><span class="sxs-lookup"><span data-stu-id="d1c8a-118">If the value of this property is not set, the session user's shell command will be run.</span></span> <span data-ttu-id="d1c8a-119">Команда Shell будет считаться из следующего значения реестра на сервере:</span><span class="sxs-lookup"><span data-stu-id="d1c8a-119">The shell command will be read from the following registry value on the server:</span></span>

<span data-ttu-id="d1c8a-120">**HKey \_ Программа локального \_ компьютера** \\ **программное обеспечение** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Shell**</span><span class="sxs-lookup"><span data-stu-id="d1c8a-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**Shell**</span></span>

<span data-ttu-id="d1c8a-121">Дополнительные сведения см. в руководстве [по обеспечению безопасности клиента RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c8a-121">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="d1c8a-122">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d1c8a-122">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c8a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d1c8a-123">Requirements</span></span>



| <span data-ttu-id="d1c8a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d1c8a-124">Requirement</span></span> | <span data-ttu-id="d1c8a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d1c8a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c8a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1c8a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c8a-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1c8a-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d1c8a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1c8a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c8a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1c8a-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d1c8a-130">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d1c8a-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1c8a-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1c8a-131"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="d1c8a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d1c8a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1c8a-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1c8a-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="d1c8a-134">IID</span><span class="sxs-lookup"><span data-stu-id="d1c8a-134">IID</span></span><br/>                      | <span data-ttu-id="d1c8a-135">IID \_ имстсксекуредсеттингс определен как c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="d1c8a-135">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1c8a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1c8a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c8a-137">**имсрдпклиентсекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="d1c8a-137">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d1c8a-138">**имстсксекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="d1c8a-138">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





