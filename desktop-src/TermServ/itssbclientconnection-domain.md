---
title: Итссбклиентконнектион, свойство домена
description: Извлекает значение, указывающее доменное имя клиента подключение к удаленному рабочему столу (RDC).
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойств домена
- Службы удаленных рабочих столов свойств домена, интерфейс Итссбклиентконнектион
- Службы удаленных рабочих столов интерфейса Итссбклиентконнектион, свойство Domain
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 678d6fc6838b615faeec9fa36b736b3105b64453
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682076"
---
# <a name="itssbclientconnectiondomain-property"></a><span data-ttu-id="84c74-106">Итссбклиентконнектион: свойство омаин:D</span><span class="sxs-lookup"><span data-stu-id="84c74-106">ITsSbClientConnection::Domain property</span></span>

<span data-ttu-id="84c74-107">Извлекает значение, указывающее доменное имя клиента подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="84c74-107">Retrieves a value that indicates the domain name of the Remote Desktop Connection (RDC) client.</span></span>

<span data-ttu-id="84c74-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="84c74-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c74-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84c74-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="84c74-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="84c74-110">Property value</span></span>

<span data-ttu-id="84c74-111">Указатель на переменную **BSTR** , содержащую доменное имя клиента RDC.</span><span class="sxs-lookup"><span data-stu-id="84c74-111">A pointer to a **BSTR** variable that contains the domain name of the RDC client.</span></span> <span data-ttu-id="84c74-112">После завершения использования строки освободите ее, вызвав функцию [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="84c74-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c74-113">Требования</span><span class="sxs-lookup"><span data-stu-id="84c74-113">Requirements</span></span>



| <span data-ttu-id="84c74-114">Требование</span><span class="sxs-lookup"><span data-stu-id="84c74-114">Requirement</span></span> | <span data-ttu-id="84c74-115">Значение</span><span class="sxs-lookup"><span data-stu-id="84c74-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="84c74-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84c74-116">Minimum supported client</span></span><br/> | <span data-ttu-id="84c74-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="84c74-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="84c74-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84c74-118">Minimum supported server</span></span><br/> | <span data-ttu-id="84c74-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84c74-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="84c74-120">IDL</span><span class="sxs-lookup"><span data-stu-id="84c74-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84c74-121"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84c74-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84c74-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84c74-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c74-123">**итссбклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="84c74-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

