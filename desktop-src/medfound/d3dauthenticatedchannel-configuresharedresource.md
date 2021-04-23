---
description: Содержит входные данные для \_ команды ШАРЕДРЕСАУРЦЕ D3DAUTHENTICATEDCONFIGURE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: Структура D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7cbbb1645b232195e1cdb12e859234339ddda287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692064"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a><span data-ttu-id="b72e7-103">\_Структура КОНФИГУРЕШАРЕДРЕСАУРЦЕ D3DAUTHENTICATEDCHANNEL</span><span class="sxs-lookup"><span data-stu-id="b72e7-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE structure</span></span>

<span data-ttu-id="b72e7-104">Содержит входные данные для [**команды \_ шаредресаурце D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-sharedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="b72e7-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) command.</span></span>

<span data-ttu-id="b72e7-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="b72e7-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="b72e7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b72e7-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a><span data-ttu-id="b72e7-107">Члены</span><span class="sxs-lookup"><span data-stu-id="b72e7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b72e7-108">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b72e7-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="b72e7-109">[**D3DAUTHENTICATEDCHANNEL \_ Настройка \_ входной**](d3dauthenticatedchannel-configure-input.md) структуры, которая содержит идентификатор GUID команды и другие данные.</span><span class="sxs-lookup"><span data-stu-id="b72e7-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="b72e7-110">**процессидентифертипе**</span><span class="sxs-lookup"><span data-stu-id="b72e7-110">**ProcessIdentiferType**</span></span>
</dt> <dd>

<span data-ttu-id="b72e7-111">Значение [**D3DAUTHENTICATEDCHANNEL \_ процессидентифиертипе**](d3dauthenticatedchannel-processidentifiertype.md) , указывающее тип процесса.</span><span class="sxs-lookup"><span data-stu-id="b72e7-111">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span> <span data-ttu-id="b72e7-112">Чтобы указать процесс диспетчер окон рабочего стола (DWM), установите для этого элемента значение **процессидтипе \_ DWM**.</span><span class="sxs-lookup"><span data-stu-id="b72e7-112">To specify the Desktop Window Manager (DWM) process, set this member to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="b72e7-113">В противном случае установите этот элемент в **процессидтипе \_ Handle** и присвойте элементу **процесшандле** допустимый маркер.</span><span class="sxs-lookup"><span data-stu-id="b72e7-113">Otherwise, set this member to **PROCESSIDTYPE\_HANDLE** and set the **ProcessHandle** member to a valid handle.</span></span>

</dd> <dt>

<span data-ttu-id="b72e7-114">**процесшандле**</span><span class="sxs-lookup"><span data-stu-id="b72e7-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b72e7-115">Обработчик процесса.</span><span class="sxs-lookup"><span data-stu-id="b72e7-115">A process handle.</span></span> <span data-ttu-id="b72e7-116">Если элемент **процессидентифиер** равен процесстидтипе, то элемент **процесшандле** указывает на обработку процесса. **\_**</span><span class="sxs-lookup"><span data-stu-id="b72e7-116">If the **ProcessIdentifier** member equals **PROCESSTIDTYPE\_HANDLE**, the **ProcessHandle** member specifies a handle to a process.</span></span> <span data-ttu-id="b72e7-117">В противном случае значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b72e7-117">Otherwise, the value is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b72e7-118">**алловакцесс**</span><span class="sxs-lookup"><span data-stu-id="b72e7-118">**AllowAccess**</span></span>
</dt> <dd>

<span data-ttu-id="b72e7-119">Если **значение — true**, указанный процесс имеет доступ к ограниченным общим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="b72e7-119">If **TRUE**, the specified process has access to restricted shared resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b72e7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b72e7-120">Requirements</span></span>



| <span data-ttu-id="b72e7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b72e7-121">Requirement</span></span> | <span data-ttu-id="b72e7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b72e7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b72e7-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b72e7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b72e7-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b72e7-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b72e7-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b72e7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b72e7-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b72e7-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b72e7-127">Header</span><span class="sxs-lookup"><span data-stu-id="b72e7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b72e7-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b72e7-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b72e7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b72e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72e7-130">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="b72e7-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="b72e7-131">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="b72e7-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




