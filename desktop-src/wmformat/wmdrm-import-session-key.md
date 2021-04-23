---
title: Структура WMDRM_IMPORT_SESSION_KEY (Дрмекстерналс. h)
description: '\_ \_ Структура ключа сеанса импорта WMDRM \_ содержит ключ сеанса для импорта защищенного содержимого.'
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- Формат WMDRM_IMPORT_SESSION_KEY структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136982"
---
# <a name="wmdrm_import_session_key-structure"></a><span data-ttu-id="abb46-105">\_ \_ Структура ключа сеанса импорта WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="abb46-105">WMDRM\_IMPORT\_SESSION\_KEY structure</span></span>

<span data-ttu-id="abb46-106">Структура **\_ \_ \_ ключа сеанса импорта WMDRM** содержит ключ сеанса для импорта защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="abb46-106">The **WMDRM\_IMPORT\_SESSION\_KEY** structure holds the session key for importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb46-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abb46-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a><span data-ttu-id="abb46-108">Члены</span><span class="sxs-lookup"><span data-stu-id="abb46-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="abb46-109">**двкэйтипе**</span><span class="sxs-lookup"><span data-stu-id="abb46-109">**dwKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="abb46-110">Тип ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="abb46-110">Session key type.</span></span> <span data-ttu-id="abb46-111">Установите для параметра WMDRM \_ KEYTYPE \_ RC4.</span><span class="sxs-lookup"><span data-stu-id="abb46-111">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="abb46-112">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="abb46-112">**cbKey**</span></span>
</dt> <dd>

<span data-ttu-id="abb46-113">Размер ключа сеанса в байтах.</span><span class="sxs-lookup"><span data-stu-id="abb46-113">Size of the session key, in bytes.</span></span> <span data-ttu-id="abb46-114">Это значение может быть таким же, насколько вам необходимо, учитывая ограничения одной операции RSA OAEP для всего сообщения (Эта структура и ключ сеанса).</span><span class="sxs-lookup"><span data-stu-id="abb46-114">This value can be as large as you need, given the limits of a single RSA OAEP operation over the entire message (this structure plus the session key).</span></span>

</dd> <dt>

<span data-ttu-id="abb46-115">**ргбкэй**</span><span class="sxs-lookup"><span data-stu-id="abb46-115">**rgbKey**</span></span>
</dt> <dd>

<span data-ttu-id="abb46-116">Адрес буфера, содержащего ключ сеанса.</span><span class="sxs-lookup"><span data-stu-id="abb46-116">Address of a buffer containing the session key.</span></span> <span data-ttu-id="abb46-117">Размер буфера должен совпадать со значением **cbKey**.</span><span class="sxs-lookup"><span data-stu-id="abb46-117">The buffer size must match the value of **cbKey**.</span></span> <span data-ttu-id="abb46-118">Данные в буфере — это значение ключа, созданное случайным образом.</span><span class="sxs-lookup"><span data-stu-id="abb46-118">The data in the buffer is a randomly generated key value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abb46-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abb46-119">Remarks</span></span>

<span data-ttu-id="abb46-120">Эта структура, включая буфер, содержащий ключ сеанса, должна быть зашифрована с помощью открытого ключа компьютера Windows Media DRM и включена в элемент **пбенкриптедсессионкэймессаже** структуры [**\_ \_ \_ структуры импорта WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="abb46-120">This structure, including the buffer containing the session key, must be encrypted with the Windows Media DRM machine public key and included in the **pbEncryptedSessionKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="abb46-121">Требования</span><span class="sxs-lookup"><span data-stu-id="abb46-121">Requirements</span></span>



| <span data-ttu-id="abb46-122">Требование</span><span class="sxs-lookup"><span data-stu-id="abb46-122">Requirement</span></span> | <span data-ttu-id="abb46-123">Значение</span><span class="sxs-lookup"><span data-stu-id="abb46-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb46-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abb46-124">Minimum supported client</span></span><br/> | <span data-ttu-id="abb46-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="abb46-125">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="abb46-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abb46-126">Minimum supported server</span></span><br/> | <span data-ttu-id="abb46-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="abb46-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="abb46-128">Версия</span><span class="sxs-lookup"><span data-stu-id="abb46-128">Version</span></span><br/>                  | <span data-ttu-id="abb46-129">Пакет SDK для Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="abb46-129">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="abb46-130">Header</span><span class="sxs-lookup"><span data-stu-id="abb46-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="abb46-131"><dt>Дрмекстерналс. h</dt></span><span class="sxs-lookup"><span data-stu-id="abb46-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abb46-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abb46-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb46-133">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="abb46-133">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





