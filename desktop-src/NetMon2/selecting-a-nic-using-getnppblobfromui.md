---
description: В сетевой монитор, выбор сетевого адаптера программным способом состоит из двух этапов. Сначала создайте большой двоичный объект фильтрации, вызвав метод CreateBlob. Затем выберите сетевой адаптер, вызвав метод Жетнппблобфромуи.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Выбор сетевого адаптера с помощью Жетнппблобфромуи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3bd02ef5085bba511fb0d05844840eb92d85ef83c67f244ab321570fae4ad8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128904"
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



 

 



