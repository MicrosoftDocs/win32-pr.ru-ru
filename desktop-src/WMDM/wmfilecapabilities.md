---
title: Структура ВМФИЛЕКАПАБИЛИТИЕС
description: Структура ВМФИЛЕКАПАБИЛИТИЕС описывает тип MIME.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Структура ВМФИЛЕКАПАБИЛИТИЕС Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694546"
---
# <a name="wmfilecapabilities-structure"></a><span data-ttu-id="1411a-104">Структура ВМФИЛЕКАПАБИЛИТИЕС</span><span class="sxs-lookup"><span data-stu-id="1411a-104">WMFILECAPABILITIES structure</span></span>

<span data-ttu-id="1411a-105">Структура **вмфилекапабилитиес** описывает тип MIME.</span><span class="sxs-lookup"><span data-stu-id="1411a-105">The **WMFILECAPABILITIES** structure describes the MIME type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1411a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1411a-106">Syntax</span></span>


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a><span data-ttu-id="1411a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1411a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1411a-108">**пвсзмиметипе**</span><span class="sxs-lookup"><span data-stu-id="1411a-108">**pwszMimeType**</span></span>
</dt> <dd>

<span data-ttu-id="1411a-109">Тип MIME.</span><span class="sxs-lookup"><span data-stu-id="1411a-109">MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="1411a-110">**двресервед**</span><span class="sxs-lookup"><span data-stu-id="1411a-110">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="1411a-111">**DWORD** зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="1411a-111">**DWORD** reserved for future use.</span></span> <span data-ttu-id="1411a-112">Установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="1411a-112">Set to zero (0).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1411a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1411a-113">Requirements</span></span>



| <span data-ttu-id="1411a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1411a-114">Requirement</span></span> | <span data-ttu-id="1411a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1411a-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1411a-116">Header</span><span class="sxs-lookup"><span data-stu-id="1411a-116">Header</span></span><br/> | <dl> <span data-ttu-id="1411a-117"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1411a-117"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1411a-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1411a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1411a-119">**IWMDMDevice2::GetFormatSupport2**</span><span class="sxs-lookup"><span data-stu-id="1411a-119">**IWMDMDevice2::GetFormatSupport2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[<span data-ttu-id="1411a-120">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="1411a-120">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





