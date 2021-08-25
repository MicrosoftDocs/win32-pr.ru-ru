---
description: Автоматически подклассы и добавляют трехмерные эффекты во все диалоговые окна приложения.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Функция Ctl3dAutoSubclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 5edc8bafb00d5444f18b61e0600fb075b6a7367c315c2ab1cfe38f911e9a84d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654614"
---
# <a name="ctl3dautosubclass-function"></a>Функция Ctl3dAutoSubclass

Автоматически подклассы и добавляют трехмерные эффекты во все диалоговые окна приложения.

## <a name="syntax"></a>Синтаксис


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хинстапп* 
</dt> <dd>

Описатель приложения, регистрируемого в качестве клиента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если не существует одно из следующих условий. в этом случае возвращается **значение false**:

-   ctl3d сегодня выполняется в Windows версии 3,0 или более ранней.
-   CTL3D сегодня не имеет свободного места в таблицах для текущего приложения. CTL3D сегодня может обслуживать до 32 приложений одновременно.
-   CTL3D сегодня не может установить свой обработчик CBT.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
