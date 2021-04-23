---
title: Структура Вмдрмкриптодата (Вмдрмсдк. h)
description: Структура Вмдрмкриптодата содержит сведения о алгоритме шифрования, который используется для шифрования и расшифровки содержимого.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Формат Windows Media структура Вмдрмкриптодата
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce972cdf41ff1e587d40b5fc95021f568be95f9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698841"
---
# <a name="wmdrmcryptodata-structure"></a><span data-ttu-id="45092-105">Структура Вмдрмкриптодата</span><span class="sxs-lookup"><span data-stu-id="45092-105">WMDRMCryptoData structure</span></span>

<span data-ttu-id="45092-106">Структура **вмдрмкриптодата** содержит сведения о алгоритме шифрования, который используется для шифрования и расшифровки содержимого.</span><span class="sxs-lookup"><span data-stu-id="45092-106">The **WMDRMCryptoData** structure contains information about the cryptographic algorithm used to encrypt and decrypt content.</span></span>

## <a name="syntax"></a><span data-ttu-id="45092-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45092-107">Syntax</span></span>


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a><span data-ttu-id="45092-108">Члены</span><span class="sxs-lookup"><span data-stu-id="45092-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="45092-109">**криптотипе**</span><span class="sxs-lookup"><span data-stu-id="45092-109">**cryptoType**</span></span>
</dt> <dd>

<span data-ttu-id="45092-110">Член перечисления [**\_ \_ типа шифрования DRM**](drm-crypto-type.md) , указывающий тип алгоритма шифрования.</span><span class="sxs-lookup"><span data-stu-id="45092-110">Member of the [**DRM\_CRYPTO\_TYPE**](drm-crypto-type.md) enumeration specifying the type of cryptographic algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="45092-111">**квкаунтерид**</span><span class="sxs-lookup"><span data-stu-id="45092-111">**qwCounterID**</span></span>
</dt> <dd>

<span data-ttu-id="45092-112">Старшие 64 бит в режиме счетчика 128-разрядного AES.</span><span class="sxs-lookup"><span data-stu-id="45092-112">The high 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="45092-113">Этот элемент используется только в том случае  , если для элемента криптотипе **задан \_ тип шифрования \_ MCE**.</span><span class="sxs-lookup"><span data-stu-id="45092-113">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> <dt>

<span data-ttu-id="45092-114">**квоффсет**</span><span class="sxs-lookup"><span data-stu-id="45092-114">**qwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="45092-115">Младшие 64 бит 128-разрядного режима счетчика AES.</span><span class="sxs-lookup"><span data-stu-id="45092-115">The low 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="45092-116">Этот элемент используется только в том случае  , если для элемента криптотипе **задан \_ тип шифрования \_ MCE**.</span><span class="sxs-lookup"><span data-stu-id="45092-116">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45092-117">Требования</span><span class="sxs-lookup"><span data-stu-id="45092-117">Requirements</span></span>



| <span data-ttu-id="45092-118">Требование</span><span class="sxs-lookup"><span data-stu-id="45092-118">Requirement</span></span> | <span data-ttu-id="45092-119">Значение</span><span class="sxs-lookup"><span data-stu-id="45092-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45092-120">Header</span><span class="sxs-lookup"><span data-stu-id="45092-120">Header</span></span><br/> | <dl> <span data-ttu-id="45092-121"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="45092-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45092-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45092-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45092-123">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="45092-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





