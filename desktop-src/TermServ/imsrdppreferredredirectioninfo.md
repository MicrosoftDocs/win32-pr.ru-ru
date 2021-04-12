---
title: Интерфейс Имсрдппреферредредиректионинфо
description: Предоставляет свойство для управления использованием сервера перенаправления.
ms.assetid: 1EAD9B15-4A84-4179-8A92-F0736B04B4F1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдппреферредредиректионинфо
- Службы удаленных рабочих столов интерфейса Имсрдппреферредредиректионинфо, описание
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8ea28c36ca06548128954298e35c0cc20de5b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489510"
---
# <a name="imsrdppreferredredirectioninfo-interface"></a><span data-ttu-id="f5dcd-105">Интерфейс Имсрдппреферредредиректионинфо</span><span class="sxs-lookup"><span data-stu-id="f5dcd-105">IMsRdpPreferredRedirectionInfo interface</span></span>

<span data-ttu-id="f5dcd-106">Предоставляет свойство для управления использованием сервера перенаправления.</span><span class="sxs-lookup"><span data-stu-id="f5dcd-106">Provides a property to control using a redirection server.</span></span>

## <a name="members"></a><span data-ttu-id="f5dcd-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="f5dcd-107">Members</span></span>

<span data-ttu-id="f5dcd-108">Интерфейс **имсрдппреферредредиректионинфо** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f5dcd-108">The **IMsRdpPreferredRedirectionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f5dcd-109">**Имсрдппреферредредиректионинфо** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f5dcd-109">**IMsRdpPreferredRedirectionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="f5dcd-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5dcd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5dcd-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5dcd-111">Properties</span></span>

<span data-ttu-id="f5dcd-112">Интерфейс **имсрдппреферредредиректионинфо** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f5dcd-112">The **IMsRdpPreferredRedirectionInfo** interface has these properties.</span></span>



| <span data-ttu-id="f5dcd-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="f5dcd-113">Property</span></span>                                                                                               | <span data-ttu-id="f5dcd-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="f5dcd-114">Access type</span></span>           | <span data-ttu-id="f5dcd-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f5dcd-115">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="f5dcd-116">**усередиректионсервернаме**</span><span class="sxs-lookup"><span data-stu-id="f5dcd-116">**UseRedirectionServerName**</span></span>](imsrdppreferredredirectioninfo-useredirectionservername.md)<br/> | <span data-ttu-id="f5dcd-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f5dcd-117">Read/write</span></span><br/> | <span data-ttu-id="f5dcd-118">Возвращает или задает значение, указывающее, следует ли использовать имя сервера перенаправления.</span><span class="sxs-lookup"><span data-stu-id="f5dcd-118">Gets and sets whether to use the redirection server name.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f5dcd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f5dcd-119">Requirements</span></span>



| <span data-ttu-id="f5dcd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f5dcd-120">Requirement</span></span> | <span data-ttu-id="f5dcd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f5dcd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5dcd-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5dcd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f5dcd-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f5dcd-123">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f5dcd-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5dcd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f5dcd-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f5dcd-125">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f5dcd-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f5dcd-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5dcd-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5dcd-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f5dcd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f5dcd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5dcd-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5dcd-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f5dcd-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="f5dcd-130">CLSID</span></span><br/>                    | <span data-ttu-id="f5dcd-131">\_MSRDPCLIENT10 CLSID определен как C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span><span class="sxs-lookup"><span data-stu-id="f5dcd-131">CLSID\_MsRdpClient10 is defined as C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span></span><br/> <span data-ttu-id="f5dcd-132">\_MSRDPCLIENT10NOTSAFEFORSCRIPTING CLSID определен как A0C63C30-F08D-4AB4-907C-34905D770C7D</span><span class="sxs-lookup"><span data-stu-id="f5dcd-132">CLSID\_MsRdpClient10NotSafeForScripting is defined as A0C63C30-F08D-4AB4-907C-34905D770C7D</span></span><br/> <span data-ttu-id="f5dcd-133">\_MSRDPCLIENT7 CLSID определен как A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="f5dcd-133">CLSID\_MsRdpClient7 is defined as A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span><br/> <span data-ttu-id="f5dcd-134">\_MSRDPCLIENT7NOTSAFEFORSCRIPTING CLSID определен как 54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="f5dcd-134">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span><br/> <span data-ttu-id="f5dcd-135">\_MSRDPCLIENT8 CLSID определен как 5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="f5dcd-135">CLSID\_MsRdpClient8 is defined as 5F681803-2900-4C43-A1CC-CF405404A676</span></span><br/> <span data-ttu-id="f5dcd-136">\_MSRDPCLIENT8NOTSAFEFORSCRIPTING CLSID определен как A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="f5dcd-136">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="f5dcd-137">\_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="f5dcd-137">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="f5dcd-138">\_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="f5dcd-138">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="f5dcd-139">IID</span><span class="sxs-lookup"><span data-stu-id="f5dcd-139">IID</span></span><br/>                      | <span data-ttu-id="f5dcd-140">IID \_ имсрдппреферредредиректионинфо определен как FDD029F9-9574-4DEF-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="f5dcd-140">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

