---
title: Свойство UserName Итссбклиентконнектион
description: Извлекает значение, указывающее имя пользователя, инициировавшего подключение.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства имени пользователя
- Свойство UserName службы удаленных рабочих столов, интерфейс Итссбклиентконнектион
- Службы удаленных рабочих столов интерфейса Итссбклиентконнектион, свойство UserName
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bd3c1e5bb588ffb276b336cd945f32a0c19afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341145"
---
# <a name="itssbclientconnectionusername-property"></a><span data-ttu-id="ca3dd-106">Свойство Итссбклиентконнектион:: UserName</span><span class="sxs-lookup"><span data-stu-id="ca3dd-106">ITsSbClientConnection::UserName property</span></span>

<span data-ttu-id="ca3dd-107">Извлекает значение, указывающее имя пользователя, инициировавшего подключение.</span><span class="sxs-lookup"><span data-stu-id="ca3dd-107">Retrieves a value that indicates the name of the user who initiated the connection.</span></span>

<span data-ttu-id="ca3dd-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ca3dd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca3dd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca3dd-109">Syntax</span></span>


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="ca3dd-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ca3dd-110">Property value</span></span>

<span data-ttu-id="ca3dd-111">Указатель на имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="ca3dd-111">A pointer to a user name.</span></span> <span data-ttu-id="ca3dd-112">После завершения использования строки освободите ее, вызвав функцию [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="ca3dd-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca3dd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ca3dd-113">Requirements</span></span>



| <span data-ttu-id="ca3dd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ca3dd-114">Requirement</span></span> | <span data-ttu-id="ca3dd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ca3dd-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca3dd-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca3dd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ca3dd-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ca3dd-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ca3dd-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca3dd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ca3dd-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ca3dd-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="ca3dd-120">IDL</span><span class="sxs-lookup"><span data-stu-id="ca3dd-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca3dd-121"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca3dd-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca3dd-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca3dd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca3dd-123">**итссбклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="ca3dd-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

