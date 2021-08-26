---
description: Метод конструктора Кпоспасссру. Кпоспасссру.
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Кпоспасссру. Кпоспасссру, конструктор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: ec75218f43edcf6c3c2c6298eba7c886cdd04879485bf41f20951cba1f9c4935
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108324"
---
# <a name="cpospassthrucpospassthru-constructor"></a>Кпоспасссру. Кпоспасссру, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Указатель на имя объекта для целей отладки. Выделите этот параметр в статической памяти.

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на владельца этого объекта. Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования. В противном случае присвойте этому параметру **значение NULL**.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на значение **HRESULT** . Не обрабатывается.

</dd> <dt>

*ппин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного ПИН-кода фильтра.

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



