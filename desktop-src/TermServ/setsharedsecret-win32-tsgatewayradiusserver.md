---
title: Метод Сетшаредсекрет класса Win32_TSGatewayRADIUSServer
description: Задает свойство SharedSecret для этого сервера протокол RADIUS (RADIUS).
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетшаредсекрет
- Службы удаленных рабочих столов метода Сетшаредсекрет, класс Win32_TSGatewayRADIUSServer
- Класс Win32_TSGatewayRADIUSServer службы удаленных рабочих столов, метод Сетшаредсекрет
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f17e22061467194bdb09fc3f2c6105706f58e587
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802926"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="b78ed-106">Метод Сетшаредсекрет \_ класса Win32 тсгатевайрадиуссервер</span><span class="sxs-lookup"><span data-stu-id="b78ed-106">SetSharedSecret method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="b78ed-107">Задает свойство **SharedSecret** для этого сервера протокол RADIUS (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="b78ed-107">Sets the **SharedSecret** property for this Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b78ed-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b78ed-108">Syntax</span></span>


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="b78ed-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b78ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b78ed-110">*SharedSecret* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b78ed-110">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b78ed-111">Новый общий секрет.</span><span class="sxs-lookup"><span data-stu-id="b78ed-111">New shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b78ed-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b78ed-112">Return value</span></span>

<span data-ttu-id="b78ed-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b78ed-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b78ed-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b78ed-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b78ed-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b78ed-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b78ed-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b78ed-116">Remarks</span></span>

<span data-ttu-id="b78ed-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="b78ed-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b78ed-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="b78ed-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b78ed-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="b78ed-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b78ed-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="b78ed-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b78ed-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b78ed-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b78ed-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b78ed-122">Requirements</span></span>



| <span data-ttu-id="b78ed-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b78ed-123">Requirement</span></span> | <span data-ttu-id="b78ed-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b78ed-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b78ed-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b78ed-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b78ed-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b78ed-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b78ed-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b78ed-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b78ed-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b78ed-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b78ed-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b78ed-129">Namespace</span></span><br/>                | <span data-ttu-id="b78ed-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b78ed-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b78ed-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b78ed-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b78ed-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b78ed-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b78ed-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b78ed-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b78ed-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b78ed-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b78ed-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b78ed-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78ed-136">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="b78ed-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

