---
title: Структура ОПАКУЕКОММАНД
description: Структура ОПАКУЕКОММАНД содержит данные для команд, которые передаются на устройство с помощью Windows Media диспетчер устройств, но не предназначены для выполнения действий диспетчер устройств Windows Media.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Структура ОПАКУЕКОММАНД Windows Media диспетчер устройств
- Структура диспетчер устройств мультимедиа Windows
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695068"
---
# <a name="opaquecommand-structure"></a><span data-ttu-id="afe97-105">Структура ОПАКУЕКОММАНД</span><span class="sxs-lookup"><span data-stu-id="afe97-105">OPAQUECOMMAND structure</span></span>

<span data-ttu-id="afe97-106">Структура **опакуекомманд** содержит данные для команд, которые передаются на устройство с помощью windows Media Диспетчер устройств, но не предназначены для выполнения действий Диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="afe97-106">The **OPAQUECOMMAND** structure contains data for commands that are passed through Windows Media Device Manager to a device but are not intended to be acted upon by Windows Media Device Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe97-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afe97-107">Syntax</span></span>


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a><span data-ttu-id="afe97-108">Члены</span><span class="sxs-lookup"><span data-stu-id="afe97-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="afe97-109">**гуидкомманд**</span><span class="sxs-lookup"><span data-stu-id="afe97-109">**guidCommand**</span></span>
</dt> <dd>

<span data-ttu-id="afe97-110">**Идентификатор GUID** , представляющий запрошенную команду.</span><span class="sxs-lookup"><span data-stu-id="afe97-110">**GUID** representing the requested command.</span></span>

</dd> <dt>

<span data-ttu-id="afe97-111">**двдатален**</span><span class="sxs-lookup"><span data-stu-id="afe97-111">**dwDataLen**</span></span>
</dt> <dd>

<span data-ttu-id="afe97-112">Длина данных, на которые указывает *pData* , в байтах.</span><span class="sxs-lookup"><span data-stu-id="afe97-112">Length of the data to which *pData* points, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="afe97-113">**pData**</span><span class="sxs-lookup"><span data-stu-id="afe97-113">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="afe97-114">Данные, необходимые для выполнения команды, и/или данные, возвращаемые командой.</span><span class="sxs-lookup"><span data-stu-id="afe97-114">Data required to execute the command, and/or data returned by the command.</span></span>

</dd> <dt>

<span data-ttu-id="afe97-115">**Абмак \[ 20\]**</span><span class="sxs-lookup"><span data-stu-id="afe97-115">**abMAC\[20\]**</span></span>
</dt> <dd>

<span data-ttu-id="afe97-116">Этот код проверки подлинности сообщений (MAC) должен включать в себя элемент **гуидкомманд** , данные, на которые указывает *пдвдатален* , и данные, на которые указывает *pData* , если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="afe97-116">This message authentication code (MAC) should include the **guidCommand** member, the data to which *pdwDataLen* points, and the data to which *pData* points, if any.</span></span> <span data-ttu-id="afe97-117">Если *pData* имеет **значение NULL**, он не должен включаться в компьютер Mac.</span><span class="sxs-lookup"><span data-stu-id="afe97-117">If *pData* is **NULL**, it must not be included in the MAC.</span></span> <span data-ttu-id="afe97-118">ВМДМ \_ Mac \_ length определяется как 20.</span><span class="sxs-lookup"><span data-stu-id="afe97-118">WMDM\_MAC\_LENGTH is defined as 20.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afe97-119">Требования</span><span class="sxs-lookup"><span data-stu-id="afe97-119">Requirements</span></span>



| <span data-ttu-id="afe97-120">Требование</span><span class="sxs-lookup"><span data-stu-id="afe97-120">Requirement</span></span> | <span data-ttu-id="afe97-121">Значение</span><span class="sxs-lookup"><span data-stu-id="afe97-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="afe97-122">Header</span><span class="sxs-lookup"><span data-stu-id="afe97-122">Header</span></span><br/> | <dl> <span data-ttu-id="afe97-123"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="afe97-123"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afe97-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afe97-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe97-125">**Имдспдевице:: Сендопакуекомманд**</span><span class="sxs-lookup"><span data-stu-id="afe97-125">**IMDSPDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="afe97-126">**Имдспстораже:: Сендопакуекоммандс**</span><span class="sxs-lookup"><span data-stu-id="afe97-126">**IMDSPStorage::SendOpaqueCommands**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="afe97-127">**Ивмдмдевице:: Сендопакуекомманд**</span><span class="sxs-lookup"><span data-stu-id="afe97-127">**IWMDMDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="afe97-128">**Ивмдмстораже:: Сендопакуекомманд**</span><span class="sxs-lookup"><span data-stu-id="afe97-128">**IWMDMStorage::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="afe97-129">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="afe97-129">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





