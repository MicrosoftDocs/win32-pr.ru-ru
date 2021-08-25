---
title: Структура ВМФИЛЕКАПАБИЛИТИЕС
description: Структура ВМФИЛЕКАПАБИЛИТИЕС описывает тип MIME.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Структура ВМФИЛЕКАПАБИЛИТИЕС Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f4852eeb7142b92c2c1a4c2073dfc70e5f6a6d74c727a7ab9e63c285796846
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903774"
---
# <a name="wmfilecapabilities-structure"></a>Структура ВМФИЛЕКАПАБИЛИТИЕС

Структура **вмфилекапабилитиес** описывает тип MIME.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a>Члены

<dl> <dt>

**пвсзмиметипе**
</dt> <dd>

Тип MIME.

</dd> <dt>

**двресервед**
</dt> <dd>

**DWORD** зарезервировано для будущего использования. Установите нулевое значение (0).

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IWMDMDevice2::GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





