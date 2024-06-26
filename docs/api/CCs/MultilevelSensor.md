# Multilevel Sensor CC

?> CommandClass ID: `0x31`

## Multilevel Sensor CC methods

### `get`

```ts
async get(): Promise<
	(MultilevelSensorValue & { type: number }) | undefined
>;

async get(
	sensorType: number,
): Promise<MultilevelSensorValue | undefined>;

async get(
	sensorType: number,
	scale: number,
): Promise<number | undefined>;
```

### `getSupportedSensorTypes`

```ts
async getSupportedSensorTypes(): Promise<
	readonly number[] | undefined
>;
```

### `getSupportedScales`

```ts
async getSupportedScales(
	sensorType: number,
): Promise<readonly number[] | undefined>;
```

### `sendReport`

```ts
async sendReport(
	sensorType: number,
	scale: number | Scale,
	value: number,
): Promise<void>;
```

## Multilevel Sensor CC values

### `value(sensorTypeName: string)`

```ts
{
	commandClass: CommandClasses["Multilevel Sensor"],
	endpoint: number,
	property: string,
}
```

-   **label:** _(dynamic)_
-   **min. CC version:** 1
-   **readable:** true
-   **writeable:** false
-   **stateful:** true
-   **secret:** false
-   **value type:** `"number"`
