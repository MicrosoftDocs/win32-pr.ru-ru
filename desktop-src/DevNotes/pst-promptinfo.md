---
description: Определяет режим запроса для защищенного хранилища при каждом отображении пользовательского интерфейса.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: Структура PST_PROMPTINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668509"
---
# <a name="pst_promptinfo-structure"></a>\_Структура PST промптинфо

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Определяет режим запроса для защищенного хранилища при каждом отображении пользовательского интерфейса.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер этой структуры.

</dd> <dt>

**двпромптфлагс**
</dt> <dd>

Этот флаг отклонен.



| Значение                                                                                                                                                                                                                                          | Значение                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> PST-файл <dt>**\_ PF \_ всегда \_ Показывать**</dt> <dt>0x00000001</dt> </dl> | Запрашивает у поставщика диалоговое окно приглашения пользователю, даже если оно не требуется для этого доступа. <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> PST-файл <dt>**\_ PF \_ никогда не \_ Показывать**</dt> <dt>0x00000002</dt> </dl>    | Не показывать диалоговое окно запроса пользователю.<br/>                                                                 |



 

</dd> <dt>

**хвндапп**
</dt> <dd>

Маркер родительского окна для пользовательского интерфейса. Элемент **хвндапп** определяет, где отображается пользовательский интерфейс. Если передается **значение NULL** , Рабочий стол считается родительским окном.

</dd> <dt>

**сзпромпт**
</dt> <dd>

Строка запроса.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**DeleteItem**](ipstore-deleteitem.md)
</dt> <dt>

[**опенитем**](ipstore-openitem.md)
</dt> <dt>

[**ReadItem**](ipstore-readitem.md)
</dt> <dt>

[**вритеитем**](ipstore-writeitem.md)
</dt> </dl>

 

 
