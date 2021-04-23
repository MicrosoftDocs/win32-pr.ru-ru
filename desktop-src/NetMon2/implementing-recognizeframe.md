---
description: Сетевые мониторы вызывают функцию Рекогнизефраме средства синтаксического анализа, чтобы определить, что средство синтаксического анализа распознает необработанные данные кадра.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Реализация Рекогнизефраме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970eee80a04168b3fa06b117c2c219c506da7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348945"
---
# <a name="implementing-recognizeframe"></a><span data-ttu-id="a2351-103">Реализация Рекогнизефраме</span><span class="sxs-lookup"><span data-stu-id="a2351-103">Implementing RecognizeFrame</span></span>

<span data-ttu-id="a2351-104">Сетевые мониторы вызывают функцию [**рекогнизефраме**](recognizeframe.md) средства синтаксического анализа, чтобы определить, что средство синтаксического анализа распознает необработанные данные кадра.</span><span class="sxs-lookup"><span data-stu-id="a2351-104">Network Monitors calls the [**RecognizeFrame**](recognizeframe.md) function of a parser to determine that the parser recognizes the unclaimed data of a frame.</span></span> <span data-ttu-id="a2351-105">Неутвержденные данные могут находиться в начале кадра, но обычно неутвержденные данные находятся в середине кадра.</span><span class="sxs-lookup"><span data-stu-id="a2351-105">The unclaimed data may be at the start of a frame, but typically, unclaimed data is located in the middle of a frame.</span></span> <span data-ttu-id="a2351-106">На следующем рисунке показаны неутвержденные данные, расположенные в середине рамки.</span><span class="sxs-lookup"><span data-stu-id="a2351-106">The following illustration shows unclaimed data located in the middle of a frame.</span></span>

![Неутвержденные данные, расположенные в середине кадра](images/recognizeframe1.png)

<span data-ttu-id="a2351-108">Сетевой монитор предоставляет следующие сведения при вызове функции [**рекогнизефраме**](recognizeframe.md) :</span><span class="sxs-lookup"><span data-stu-id="a2351-108">Network Monitor provides the following information when it calls the [**RecognizeFrame**](recognizeframe.md) function:</span></span>

-   <span data-ttu-id="a2351-109">Маркер фрейма.</span><span class="sxs-lookup"><span data-stu-id="a2351-109">A handle to the frame.</span></span>
-   <span data-ttu-id="a2351-110">Указатель на начало кадра.</span><span class="sxs-lookup"><span data-stu-id="a2351-110">A pointer to the start of the frame.</span></span>
-   <span data-ttu-id="a2351-111">Указатель на начало неутвержденных данных.</span><span class="sxs-lookup"><span data-stu-id="a2351-111">A pointer to the start of the unclaimed data.</span></span>
-   <span data-ttu-id="a2351-112">Значение MAC первого протокола в кадре.</span><span class="sxs-lookup"><span data-stu-id="a2351-112">The MAC value of the first protocol in the frame.</span></span>
-   <span data-ttu-id="a2351-113">Число байтов в неутвержденных данных; то есть байты, оставшиеся в кадре.</span><span class="sxs-lookup"><span data-stu-id="a2351-113">The number of bytes in the unclaimed data; that is, the bytes remaining in the frame.</span></span>
-   <span data-ttu-id="a2351-114">Обработчик предыдущего протокола.</span><span class="sxs-lookup"><span data-stu-id="a2351-114">A handle to the previous protocol.</span></span>
-   <span data-ttu-id="a2351-115">Смещение предыдущего протокола.</span><span class="sxs-lookup"><span data-stu-id="a2351-115">The offset of the previous protocol.</span></span>

<span data-ttu-id="a2351-116">Если библиотека DLL средства синтаксического анализа определяет, что необработанные данные начинаются с протокола синтаксического анализа, то библиотека DLL синтаксического анализатора определяет, где запускается следующий протокол, и какой протокол следует за ним.</span><span class="sxs-lookup"><span data-stu-id="a2351-116">When the parser DLL determines that unclaimed data starts with the parser protocol, the parser DLL determines where the next protocol starts, and which protocol follows.</span></span> <span data-ttu-id="a2351-117">Библиотека DLL средства синтаксического анализа выполняет следующие условные действия:</span><span class="sxs-lookup"><span data-stu-id="a2351-117">The parser DLL functions in the following conditional ways:</span></span>

-   <span data-ttu-id="a2351-118">Если библиотека DLL анализатора распознает необработанные данные, DLL-файл синтаксического анализатора устанавливает параметр *ппротоколстатус* и возвращает указатель на следующий протокол в кадре или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a2351-118">If the parser DLL recognizes unclaimed data, the parser DLL sets the *pProtocolStatus* parameter, and returns a pointer to either the next protocol in the frame, or **NULL**.</span></span> <span data-ttu-id="a2351-119">**Значение NULL** возвращается, если текущий протокол является последним в кадре.</span><span class="sxs-lookup"><span data-stu-id="a2351-119">**NULL** is returned if the current protocol is the last protocol in the frame.</span></span>
-   <span data-ttu-id="a2351-120">Если библиотека DLL анализатора распознает необработанные данные и определяет протокол, указанный ниже (из сведений, предоставленных протоколом), то DLL-файл синтаксического анализатора возвращает указатель на маркер следующего протокола в параметре *фнекстпротокол* функции.</span><span class="sxs-lookup"><span data-stu-id="a2351-120">If the parser DLL recognizes unclaimed data and identifies the protocol that follows (from information provided in the protocol), then the parser DLL returns a pointer to the handle of the next protocol in the *phNextProtocol* parameter of the function.</span></span>
-   <span data-ttu-id="a2351-121">Если DLL-файл синтаксического анализатора не распознает необработанные данные, Библиотека DLL средства синтаксического анализа возвращает указатель на начало необработанных данных, а сетевой монитор продолжит попытки выполнить синтаксический анализ необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="a2351-121">If the parser DLL does not recognize unclaimed data, the parser DLL returns the pointer to the start of unclaimed data, and Network Monitor continues trying to parse the unclaimed data.</span></span>

<span data-ttu-id="a2351-122">**Реализация Рекогнизефраме**</span><span class="sxs-lookup"><span data-stu-id="a2351-122">**To implement RecognizeFrame**</span></span>

1.  <span data-ttu-id="a2351-123">Протестируйте, чтобы определить, что вы распознаете протокол.</span><span class="sxs-lookup"><span data-stu-id="a2351-123">Test to determine that you recognize the protocol.</span></span>
2.  <span data-ttu-id="a2351-124">Если вы распознаете ненужные данные и знаете, какой протокол следует, установите для параметра *ппротоколстатус* \_ состояние протокола \_ следующий \_ протокол, установите *фнекстпротокол* на указатель, указывающий на маркер для следующего протокола, а затем верните указатель на следующий протокол.</span><span class="sxs-lookup"><span data-stu-id="a2351-124">If you recognize unclaimed data and you know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_NEXT\_PROTOCOL, set *phNextProtocol* to a pointer that points to the handle for the next protocol, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="a2351-125">–или–</span><span class="sxs-lookup"><span data-stu-id="a2351-125">–or–</span></span>

    <span data-ttu-id="a2351-126">Если вы распознаете ненужные данные и не знаете, какой протокол следует, установите *ппротоколстатус* в \_ состояние протокола \_ , а затем верните указатель на следующий протокол.</span><span class="sxs-lookup"><span data-stu-id="a2351-126">If you recognize unclaimed data and you do not know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_RECOGNIZED, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="a2351-127">–или–</span><span class="sxs-lookup"><span data-stu-id="a2351-127">–or–</span></span>

    <span data-ttu-id="a2351-128">Если вы распознаете ненужные данные, а протокол является последним протоколом в кадре, установите *ппротоколстатус* в \_ состояние протокола \_ затребован, а затем возвратите **null**.</span><span class="sxs-lookup"><span data-stu-id="a2351-128">If you recognize unclaimed data and your protocol is the last protocol in a frame, set *pProtocolStatus* to PROTOCOL\_STATUS\_CLAIMED, and then return **NULL**.</span></span>

    <span data-ttu-id="a2351-129">–или–</span><span class="sxs-lookup"><span data-stu-id="a2351-129">–or–</span></span>

    <span data-ttu-id="a2351-130">Если не удается распознать ненужные данные, установите *ппротоколстатус* в \_ состояние протокола \_ не \_ распознано, а затем верните указатель, который передается вам в *ппротокол*.</span><span class="sxs-lookup"><span data-stu-id="a2351-130">If you do not recognize unclaimed data, set *pProtocolStatus* to PROTOCOL\_STATUS\_NOT\_RECOGNIZED, and then return the pointer that is passed to you in *pProtocol*.</span></span>

<span data-ttu-id="a2351-131">Ниже приведена базовая реализация [**рекогнизефраме**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="a2351-131">The following is a basic implementation of [**RecognizeFrame**](recognizeframe.md).</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



