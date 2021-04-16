---
description: Задает уровень шифрования, который выполняется перед тем, как защищенное содержимое становится доступным для ЦП или шины.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8b624c26c81549372e0e09b4a08ce73f6cd3dd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539596"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a><span data-ttu-id="77caf-103">D3DAUTHENTICATEDCONFIGURE \_ енкриптионвхенакцессибле</span><span class="sxs-lookup"><span data-stu-id="77caf-103">D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="77caf-104">Задает уровень шифрования, который выполняется перед тем, как защищенное содержимое становится доступным для ЦП или шины.</span><span class="sxs-lookup"><span data-stu-id="77caf-104">Sets the level of encryption that is performed before protected content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="77caf-105">Требование</span><span class="sxs-lookup"><span data-stu-id="77caf-105">Requirement</span></span> | <span data-ttu-id="77caf-106">Значение</span><span class="sxs-lookup"><span data-stu-id="77caf-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77caf-107">Идентификатор GUID команды</span><span class="sxs-lookup"><span data-stu-id="77caf-107">Command GUID</span></span> | <span data-ttu-id="77caf-108">**D3DAUTHENTICATEDCONFIGURE \_ енкриптионвхенакцессибле**</span><span class="sxs-lookup"><span data-stu-id="77caf-108">**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**</span></span>                                                                     |
| <span data-ttu-id="77caf-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="77caf-109">Input data</span></span>   | [<span data-ttu-id="77caf-110">**D3DAUTHENTICATEDCHANNEL \_ конфигуреункомпресседенкриптион**</span><span class="sxs-lookup"><span data-stu-id="77caf-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION**</span></span>](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

## <a name="remarks"></a><span data-ttu-id="77caf-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77caf-111">Remarks</span></span>

<span data-ttu-id="77caf-112">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="77caf-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="77caf-113">**\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="77caf-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="77caf-114">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="77caf-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="77caf-115">Требования</span><span class="sxs-lookup"><span data-stu-id="77caf-115">Requirements</span></span>



| <span data-ttu-id="77caf-116">Требование</span><span class="sxs-lookup"><span data-stu-id="77caf-116">Requirement</span></span> | <span data-ttu-id="77caf-117">Значение</span><span class="sxs-lookup"><span data-stu-id="77caf-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77caf-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77caf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="77caf-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="77caf-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="77caf-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77caf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="77caf-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="77caf-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="77caf-122">Header</span><span class="sxs-lookup"><span data-stu-id="77caf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="77caf-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="77caf-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77caf-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77caf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77caf-125">Защита содержимого команды</span><span class="sxs-lookup"><span data-stu-id="77caf-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="77caf-126">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="77caf-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="77caf-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="77caf-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




