---
description: В сетевой монитор, выбор сетевого адаптера программным способом состоит из двух этапов. Сначала создайте большой двоичный объект фильтрации, вызвав метод CreateBlob. Затем выберите сетевой адаптер, вызвав метод Жетнппблобфромуи.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Выбор сетевого адаптера с помощью Жетнппблобфромуи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb429a87d284a5a6a03a20357728c8bbcb5acac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673329"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a>Выбор сетевого адаптера с помощью Жетнппблобфромуи

В сетевой монитор, выбор сетевого адаптера программным способом состоит из двух этапов. Сначала создайте большой двоичный объект фильтрации, вызвав метод [**CreateBlob**](createblob.md) . Затем выберите сетевой адаптер, вызвав метод [**жетнппблобфромуи**](getnppblobfromui.md) .

В этом примере для выбора требуемого сетевого адаптера используется большой двоичный объект фильтра:


```C++
DWORD rc;

// Call CreateBlob to create a filter blob.
///////////////////////////////////////////
HBLOB hFilterBlob;
rc = CreateBlob(&hFilterBlob);
if (FAILED (rc));
{
  // Failed creating filter BLOB. Add appropriate error handling.
}


// Call GetNPPBlobFromUI to retrieve the NPP Blob.
//////////////////////////////////////////////////
rc = GetNPPBlobFromUI(hwnd,
                      hFilterBlob,
                      &hBlob);
if (FAILED (rc));
{
  // Failed retrieving NPP BLOB. Add appropriate error handling.
}
```



 

 



