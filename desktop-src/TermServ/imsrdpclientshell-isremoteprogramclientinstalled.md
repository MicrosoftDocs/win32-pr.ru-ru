---
title: Имсрдпклиентшелл Исремотепрограмклиентинсталлед, свойство
description: Получает значение, указывающее, поддерживает ли клиент подключение к удаленному рабочему столу (RDC) функции RemoteApp в Windows Server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Исремотепрограмклиентинсталлед
- Службы удаленных рабочих столов свойства Исремотепрограмклиентинсталлед, интерфейс Имсрдпклиентшелл
- Службы удаленных рабочих столов интерфейса Имсрдпклиентшелл, свойство Исремотепрограмклиентинсталлед
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135503"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a><span data-ttu-id="df248-106">Свойство Имсрдпклиентшелл:: Исремотепрограмклиентинсталлед</span><span class="sxs-lookup"><span data-stu-id="df248-106">IMsRdpClientShell::IsRemoteProgramClientInstalled property</span></span>

<span data-ttu-id="df248-107">Получает значение, указывающее, поддерживает ли клиент подключение к удаленному рабочему столу (RDC) функции RemoteApp в Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="df248-107">Retrieves whether the Remote Desktop Connection (RDC) client supports Windows Server 2008 R2 RemoteApp functionality.</span></span>

<span data-ttu-id="df248-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="df248-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="df248-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df248-109">Syntax</span></span>


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a><span data-ttu-id="df248-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="df248-110">Property value</span></span>

<span data-ttu-id="df248-111">Возвращает значение, указывающее, поддерживает ли клиент подключение к удаленному рабочему столу (RDC) функции RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="df248-111">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="df248-112">Требования</span><span class="sxs-lookup"><span data-stu-id="df248-112">Requirements</span></span>



| <span data-ttu-id="df248-113">Требование</span><span class="sxs-lookup"><span data-stu-id="df248-113">Requirement</span></span> | <span data-ttu-id="df248-114">Значение</span><span class="sxs-lookup"><span data-stu-id="df248-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df248-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df248-115">Minimum supported client</span></span><br/> | <span data-ttu-id="df248-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df248-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="df248-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df248-117">Minimum supported server</span></span><br/> | <span data-ttu-id="df248-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df248-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="df248-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="df248-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="df248-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df248-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="df248-121">DLL</span><span class="sxs-lookup"><span data-stu-id="df248-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df248-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df248-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="df248-123">IID</span><span class="sxs-lookup"><span data-stu-id="df248-123">IID</span></span><br/>                      | <span data-ttu-id="df248-124">IID \_ имсрдпклиентшелл определен как d012ae6d-c19a-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="df248-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="df248-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df248-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df248-126">**имсрдпклиентшелл**</span><span class="sxs-lookup"><span data-stu-id="df248-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





