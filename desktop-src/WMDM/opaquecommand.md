---
title: Структура ОПАКУЕКОММАНД
description: структура опакуекомманд содержит данные для команд, которые передаются на устройство с помощью Windows мультимедиа диспетчер устройств, но не предназначены для обработки Windows Media диспетчер устройств.
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
ms.openlocfilehash: 76d3f0b94146262c480e7e510497111bf82f0c020001717cb0000ee4a88df440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904014"
---
# <a name="opaquecommand-structure"></a>Структура ОПАКУЕКОММАНД

структура **опакуекомманд** содержит данные для команд, которые передаются на устройство с помощью Windows мультимедиа диспетчер устройств, но не предназначены для обработки Windows Media диспетчер устройств.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**гуидкомманд**
</dt> <dd>

**Идентификатор GUID** , представляющий запрошенную команду.

</dd> <dt>

**двдатален**
</dt> <dd>

Длина данных, на которые указывает *pData* , в байтах.

</dd> <dt>

**pData**
</dt> <dd>

Данные, необходимые для выполнения команды, и/или данные, возвращаемые командой.

</dd> <dt>

**Абмак \[ 20\]**
</dt> <dd>

Этот код проверки подлинности сообщений (MAC) должен включать в себя элемент **гуидкомманд** , данные, на которые указывает *пдвдатален* , и данные, на которые указывает *pData* , если таковые имеются. Если *pData* имеет **значение NULL**, он не должен включаться в компьютер Mac. ВМДМ \_ Mac \_ length определяется как 20.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Имдспдевице:: Сендопакуекомманд**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[**Имдспстораже:: Сендопакуекоммандс**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[**Ивмдмдевице:: Сендопакуекомманд**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[**Ивмдмстораже:: Сендопакуекомманд**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





