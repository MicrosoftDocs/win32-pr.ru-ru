---
description: Этот метод возвращает интерфейс, предоставляющий доступ к звуковым данным.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'Метод Иаудиофраменативе:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145133"
---
# <a name="iaudioframenativegetdata-method"></a><span data-ttu-id="0dd96-103">Метод Иаудиофраменативе:: GetData</span><span class="sxs-lookup"><span data-stu-id="0dd96-103">IAudioFrameNative::GetData method</span></span>

<span data-ttu-id="0dd96-104">Этот метод возвращает интерфейс, предоставляющий доступ к звуковым данным.</span><span class="sxs-lookup"><span data-stu-id="0dd96-104">This method returns an interface that provides access to the audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd96-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dd96-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="0dd96-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dd96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dd96-107">*riid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0dd96-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd96-108">Тип: **рефиид**</span><span class="sxs-lookup"><span data-stu-id="0dd96-108">Type: **REFIID**</span></span>

<span data-ttu-id="0dd96-109">IID получаемого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0dd96-109">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0dd96-110">*ППВ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0dd96-110">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd96-111">Тип: \**лпвоид \** _</span><span class="sxs-lookup"><span data-stu-id="0dd96-111">Type: \**LPVOID\** _</span></span>

<span data-ttu-id="0dd96-112">При успешном возврате этого метода содержит указатель интерфейса, запрошенный в параметре _riid \*.</span><span class="sxs-lookup"><span data-stu-id="0dd96-112">When this method returns successfully, contains the interface pointer requested in _riid\* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dd96-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dd96-113">Return value</span></span>

<span data-ttu-id="0dd96-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0dd96-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0dd96-115">Возвращает \_ ОК при успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="0dd96-115">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="0dd96-116">Возвращает E \_ Interface, если не удается найти запрошенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0dd96-116">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="0dd96-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0dd96-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd96-118">**иаудиофраменативе**</span><span class="sxs-lookup"><span data-stu-id="0dd96-118">**IAudioFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



