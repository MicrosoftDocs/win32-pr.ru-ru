---
title: IWMDRMDevice2 Жетпартиалсинклист, метод
description: Метод Жетпартиалсинклист получает список частичной синхронизации.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Метод Жетпартиалсинклист Windows Media диспетчер устройств
- Метод Жетпартиалсинклист Windows Media диспетчер устройств, интерфейс IWMDRMDevice2
- Интерфейс IWMDRMDevice2 Windows Media диспетчер устройств, метод Жетпартиалсинклист
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699065"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>Метод IWMDRMDevice2:: Жетпартиалсинклист

Метод **жетпартиалсинклист** получает список частичной синхронизации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кминкаунтсрешолд* \[ окне\]
</dt> <dd>

Пороговое значение минимального числа.

</dd> <dt>

*кминхаурссрешолд* \[ окне\]
</dt> <dd>

Минимальное пороговое значение часов.

</dd> <dt>

*двстартингиндекс* \[ окне\]
</dt> <dd>

Начальное расположение для индексирования.

</dd> <dt>

*Цитемс* \[ окне\]
</dt> <dd>

Число индексируемых элементов.

</dd> <dt>

*ппбсинклист* \[ заполняет\]
</dt> <dd>

Получен список синхронизации лицензий.

</dd> <dt>

*пкбсинклист* \[ заполняет\]
</dt> <dd>

Размер списка синхронизации лицензий в байтах.

</dd> <dt>

*пдвнекстстартингиндекс* \[ заполняет\]
</dt> <dd>

Следующее начальное расположение для индексирования.

</dd> <dt>

*пЦитемспроцессед* \[ заполняет\]
</dt> <dd>

Количество обрабатываемых элементов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Все методы интерфейса в диспетчер устройств Windows Media могут возвращать любой из следующих классов кодов ошибок:

-   Стандартные коды ошибок COM
-   Коды ошибок Windows преобразованы в значения HRESULT
-   Коды ошибок Windows Media диспетчер устройств

Расширенный список возможных кодов ошибок см. в разделе [коды ошибок](error-codes.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ВМДДРМСП. idl</dt> </dl> |
| Библиотека<br/> | <dl> <dt>Мссачлп. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ивмдрмдевице:: Жетсинклист**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**Интерфейс IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





