---
title: Структура ВМДМИД
description: Структура ВМДМИД описывает серийные номера и идентификаторы групп.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Структура ВМДМИД Windows Media диспетчер устройств
- Указатель структуры ПВМДМИД Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93079b2b32dae918e1c7f5c7756a1c24dd29c539c6b760dc698273006ae30f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583997"
---
# <a name="wmdmid-structure"></a>Структура ВМДМИД

Структура **вмдмид** описывает серийные номера и идентификаторы групп.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер структуры **вмдмид** в байтах.

</dd> <dt>

**дввендорид**
</dt> <dd>

Значение **типа DWORD** , содержащее зарегистрированный идентификатор поставщика. Содержит ноль, если не используется.

</dd> <dt>

**\[Длина pID вмдмид \_\]**
</dt> <dd>

Указатель на массив байтов, содержащий серийный номер. Серийный номер — это строка байтовых значений, не имеющая стандартного формата. Обратите внимание, что это значение не является расширенным символом. **Вмдмид \_ LENGTH** — это постоянное значение, определенное в мсвмдм. h.

</dd> <dt>

**сериалнумберленгс**
</dt> <dd>

Фактическая длина возвращенного серийного номера в байтах.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Имдспдевице:: Жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[**Имдспсторажеглобалс:: Жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[**Ивмдмдевице:: Жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[**Ивмдмсторажеглобалс:: Жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





