---
title: Структура WMDRM_IMPORT_CONTENT_KEY (Дрмекстерналс. h)
description: '\_ \_ Структура ключа содержимого для импорта WMDRM \_ хранит ключ содержимого, используемый при импорте защищенного содержимого.'
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- Формат WMDRM_IMPORT_CONTENT_KEY структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414865"
---
# <a name="wmdrm_import_content_key-structure"></a><span data-ttu-id="93a78-105">\_ \_ Структура ключа содержимого для импорта WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="93a78-105">WMDRM\_IMPORT\_CONTENT\_KEY structure</span></span>

<span data-ttu-id="93a78-106">Структура **\_ \_ \_ ключа содержимого для импорта WMDRM** хранит ключ содержимого, используемый при импорте защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="93a78-106">The **WMDRM\_IMPORT\_CONTENT\_KEY** structure stores the content key used in importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="93a78-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93a78-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a><span data-ttu-id="93a78-108">Члены</span><span class="sxs-lookup"><span data-stu-id="93a78-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="93a78-109">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="93a78-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="93a78-110">Версия.</span><span class="sxs-lookup"><span data-stu-id="93a78-110">Version.</span></span>

</dd> <dt>

<span data-ttu-id="93a78-111">**кбструктсизе**</span><span class="sxs-lookup"><span data-stu-id="93a78-111">**cbStructSize**</span></span>
</dt> <dd>

<span data-ttu-id="93a78-112">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="93a78-112">Size of structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="93a78-113">**двивкэйтипе**</span><span class="sxs-lookup"><span data-stu-id="93a78-113">**dwIVKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="93a78-114">Тип ключа вектора инициализации.</span><span class="sxs-lookup"><span data-stu-id="93a78-114">Initialization vector key type.</span></span> <span data-ttu-id="93a78-115">Установите для параметра WMDRM \_ KEYTYPE \_ RC4.</span><span class="sxs-lookup"><span data-stu-id="93a78-115">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="93a78-116">**кбивкэй**</span><span class="sxs-lookup"><span data-stu-id="93a78-116">**cbIVKey**</span></span>
</dt> <dd>

<span data-ttu-id="93a78-117">Размер ключа вектора инициализации в байтах.</span><span class="sxs-lookup"><span data-stu-id="93a78-117">Size of the initialization vector key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="93a78-118">**двконтенткэйтипе**</span><span class="sxs-lookup"><span data-stu-id="93a78-118">**dwContentKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="93a78-119">Тип ключа содержимого.</span><span class="sxs-lookup"><span data-stu-id="93a78-119">Content key type.</span></span> <span data-ttu-id="93a78-120">Задайте значение WMDRM \_ KEYTYPE \_ коктейль.</span><span class="sxs-lookup"><span data-stu-id="93a78-120">Set to WMDRM\_KEYTYPE\_COCKTAIL.</span></span>

</dd> <dt>

<span data-ttu-id="93a78-121">**кбконтенткэй**</span><span class="sxs-lookup"><span data-stu-id="93a78-121">**cbContentKey**</span></span>
</dt> <dd>

<span data-ttu-id="93a78-122">Размер ключа содержимого в байтах.</span><span class="sxs-lookup"><span data-stu-id="93a78-122">Size of the content key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="93a78-123">**ргбкэйдата**</span><span class="sxs-lookup"><span data-stu-id="93a78-123">**rgbKeyData**</span></span>
</dt> <dd>

<span data-ttu-id="93a78-124">Адрес буфера, содержащего ключ содержимого.</span><span class="sxs-lookup"><span data-stu-id="93a78-124">Address of a buffer containing the content key.</span></span> <span data-ttu-id="93a78-125">Размер буфера должен совпадать со значением **кбконтенткэй**.</span><span class="sxs-lookup"><span data-stu-id="93a78-125">The buffer size must match the value of **cbContentKey**.</span></span> <span data-ttu-id="93a78-126">Этот ключ должен соответствовать ключу, импортированному из сообщения лицензии КСМР.</span><span class="sxs-lookup"><span data-stu-id="93a78-126">This key should match the key imported from the XMR license message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93a78-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93a78-127">Remarks</span></span>

<span data-ttu-id="93a78-128">Эта структура, включая буфер, содержащий ключ сеанса, должна быть зашифрована с помощью ключа сеанса и включена в элемент **пбенкриптедкэймессаже** структуры [**\_ \_ \_ структуры импорта WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="93a78-128">This structure, including the buffer containing the session key, must be encrypted with the session key and included in the **pbEncryptedKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="93a78-129">Требования</span><span class="sxs-lookup"><span data-stu-id="93a78-129">Requirements</span></span>



| <span data-ttu-id="93a78-130">Требование</span><span class="sxs-lookup"><span data-stu-id="93a78-130">Requirement</span></span> | <span data-ttu-id="93a78-131">Значение</span><span class="sxs-lookup"><span data-stu-id="93a78-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a78-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93a78-132">Minimum supported client</span></span><br/> | <span data-ttu-id="93a78-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="93a78-133">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="93a78-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93a78-134">Minimum supported server</span></span><br/> | <span data-ttu-id="93a78-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93a78-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="93a78-136">Версия</span><span class="sxs-lookup"><span data-stu-id="93a78-136">Version</span></span><br/>                  | <span data-ttu-id="93a78-137">Пакет SDK для Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="93a78-137">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="93a78-138">Header</span><span class="sxs-lookup"><span data-stu-id="93a78-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="93a78-139"><dt>Дрмекстерналс. h</dt></span><span class="sxs-lookup"><span data-stu-id="93a78-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93a78-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93a78-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a78-141">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="93a78-141">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





